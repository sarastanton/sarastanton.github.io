---
layout: post
title:      "Bookable (Rails + JavaScript Project) "
date:       2018-12-16 21:30:09 -0500
permalink:  bookable_rails_javascript_project
---

Bookable - now with 100% more JavaScript!


**OVERVIEW**

For this project, I was tasked with adding JavaScript and AJAX to my [Rails project](http://codename-sara.com/ruby_on_rails_project_-_bookable). Since I would be working from a project I had already built, I thought that this time around wouldn’t be as complicated as the projects…oh man, was I wrong. In order to incorporate JavaScript and AJAX into my Rails project, there were three main things I needed to do:

1. Set up backend to serve data in JSON format to frontend

     * *Decide what does and what does not need to be serialized* - I wasn’t going to be making AJAX requests (directly or through associations) for Sessions or Read_statuses, so there was no need to serialize them. I would, however, definitely need Books, Authors, Genres, Reviews, and Ratings.

     * ActiveModel Serializers made associations for my serialized data a breeze, and they can even serialize data from custom methods (more on this in a moment!)

2. Set up AJAX requests to obtain serialized JSON data from my Rails backend (and, in a few cases, send data to the backend)

3. Use JavaScript/jQuery to target elements on the DOM and inject JSON data (obtained in step #2) into those elements

No small feat!

You can watch a video walkthrough [here](https://youtu.be/69wJBJeiaD4).


**WHAT I LEARNED**

* **Serializers** - ActiveModel Serializer is already very powerful, but learning that I could add my own methods was a game changer. For example, each Book can have many Ratings, and I needed to be able to calculate an average rating for each book. This was fine in Rails as I could use ERB to calculate the rating right on the view page - but how was I supposed to do this with JavaScript? Answer: I didn't need to have JavaScript calculate it at all! Instead, I wrote a method in the Books Serializer that calculated the average of all ratings for a particular book, then serialized and fed that data to the JavaScript front end through an AJAX request. GAME = CHANGED.

* **JavaScript Debugging** - I am very comfortable at this point with debugging in both Rails and JavaScript at this point. The debugger built into JavaScript is great to work with. It is very similar to Pry in that you add a ```debugger``` line to your code at the point where you want to pause and drop in, and you can see a real-time snapshot right in your browser console. An added benefit is that you can see what local variable values are (including ```this```, ```event.target```, etc.). In addition to the debugger, there is ```console.log()``` to display data in the browser console, and popup alert boxes that are especially handy for testing listeners, click events, etc. These tools can be can also be used to tell if a given line of code is even firing in the first place (for example, an expression within an if/then statement). Of course, you can also use Pry to see what is being passed into params, whether an AJAX request has hit the correction action within the correct controller, etc. 

* **Listeners** - You can use listeners to detect different events (such as a click, hover, keystroke, or scroll) and then "hijack" those events to do something (such as make an AJAX call, change text, or pop up an alert). Links don't have to be links, buttons don't have to be buttons...the possibilities are endless.

* **Turbolinks** - I was having a few issues with JavaScript behaving in unexpected ways when loading pages. After doing some research, I figured out that this was being caused by Turbolinks, and I was able to disable it.

* **Custom controller actions**  - Similar to my average rating conundrum, I could not call model logic directly in the view (which is not best practice anyway), so I created a few custom controller actions outside of the normal seven CRUD actions (new, create, index, show, edit, update, and destroy). This way, my JS frontend view was able to ask the *controller* for model logic, rather than needing to go to the model directly. This really helped reinforce my understanding of the MVC model (ex: mark as read)


**REFACTOR LIST**

I have a working product that functions as intended, but is not the best it can be. You could say I'm currently in the "green" phase of the "[red/green/refactor](https://www.codecademy.com/articles/tdd-red-green-refactor)" method. Here are a few things I'd like to come back to at some point:

* **JS tests** - Since I was working with my existing Rails project, I already had the RSpec tests I had written earlier for Bookable. I’d like to come back and add a few JavaScript tests as well after I learn more about them. 

* **Performance** - Right now, the Book index page takes a second or two to load. I need to figure out how to increase the load speed - perhaps I need to add back Turbolinks? 

* **Visual improvements** - As I learn more about working in the frontend (and especially with JavaScript and CSS), I want to come back and make Bookable even more visually appealing.

* **Readability/DRY** - Right now, many of my domain model objects (users, books, authors, genres, etc) run JavaScript that is very similar but contained in separate files - very much in violation of the DRY principle. It would be great to see if there are places in my code that can be rewritten to apply to all models, rather than being repeated for each one.

I’m thrilled with how this project turned out - it’s easy to see how using AJAX requests and JavaScript to read and write data without a page refresh enhances the user experience. Adding these new tools to my skill set has opened the door to a whole world of opportunity - pulling data from external APIs with AJAX, for example, or all of the things that can be done with the click of a mouse and the right listener. 

Check out the newest version of Bookable [here](https://github.com/sarastanton/bookable_w_JS)!
