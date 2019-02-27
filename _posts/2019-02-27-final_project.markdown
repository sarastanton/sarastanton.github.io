---
layout: post
title:      "FINAL PROJECT"
date:       2019-02-27 07:12:15 -0500
permalink:  final_project
---

I MADE IT!!

![Finish Line](http://1dmkak43dtkvwxzekd5zqsgk8-wpengine.netdna-ssl.com/wp-content/uploads/2015/12/finish-line.gif)

I’ve finished my final project, which puts me not just at the end of the Full Stack Web Developer program but also at the beginning of my next chapter. I remember wondering  many times during the program whether or not I would be able to make it all the way through - if I actually was capable of  learning Ruby,  Sinatra, SQL, Rails, HTML, CSS, JavaScript, React, and Redux - and I am able to look back now knowing that the answer was YES. 

On to the project itself...

For my final(!) project, I built a [meal planner](https://github.com/sarastanton/meal-planner) with CRUD functionality handled by Rails and served up with an API to the React front end. State is managed by Redux, and async calls are made with the help of Thunx middleware. I also used basic CSS and JavaScript for styling. Definitely a comprehensive project - I used nearly every skill I learned in the FSWD program!

**WHAT I LEARNED**

* **Thinking in React** - thinking of the UI in terms of components (which I tend to group into containers and cards, though this is not always how it works out) was a new concept that I actually really enjoy. If you haven’t read this short [“Thinking In React”](https://reactjs.org/docs/thinking-in-react.html) primer in the React docs, it is very much a worthwhile read.

* **State** - The concept of state has been an absolute GAME CHANGER. One of the most impactful (and possibly most obvious) ways to use state is to store data retrieved from an API; however, one of my favorite ways to use state is to toggle values (true/false, enabled/disabled, checked/unchecked) or text (button labels from “Edit” to “Save”, etc.).

* **Redux** - I wasn’t initially convinced that the hassle was worth it when component state seemed to work just fine, but I quickly saw that my project was actually a great use case for Redux because I had multiple child components that needed to access the same state data but did not share a common parent. Without Redux, I would have had to find a way to pass state data up (through props callbacks) and down through multiple components and possibly wrap together components into a container that otherwise did not need to be related at all.

*  **Redux Chrome extension** - I was hesitant at first to use this tool (side note: what was it about Redux that made me so reluctant??), as there are a few additional steps required for initial setup, but it proved to be absolutely invaluable. Recommend 1000%.

* **Styling** - I dabbled a bit with some styling in my [last project](http://codename-sara.com/bookable_rails_javascript_project), but there is quite a bit more styling in this project. I’m particularly in love with the chalkboard 😍 One thing that helped with styling at the beginning of the project was to lay out all components and containers together on one page to see how everything fit together, which components went inside which containers, etc. Each container and component rendered its own title (ex: “I am the Recipe Container”), and I formatted all containers with a box border and all “card” components with a background color to help visualize even further.  

**REFACTOR LIST**

Just like last time, I have a list of features I felt were out of scope for this current iteration of my project but would love to come back to later:


* **DEPLOY!** - #1 on my list of things to do next for this project is to deploy it to a live website (my first time ever doing so for a dynamic web app)

* **User accounts/auth** - it would be great to add user accounts (with regular old username/passwords as well as OAuth) so that users can save their own personal meal plans and recipes saved for later (especially once deployed)

* **Ingredient grouping** - the shopping list feature currently lists each individual item, allowing for duplicates. For example, if I want to make a recipe that calls for 1/2 units of X ingredient, and another recipe that calls for 3/4 units of X ingredient, it would be much nicer to see one line for 1 1/4 units of X on the shopping list rather than two separate lines.

* **DRY** - In keeping with the “red/green/refactor” approach and balancing the getting-it-done vs. falling-down-endless-rabbit-holes approaches (the latter two of which I might have just coined on the spot), there are a few parts of my code that could benefit from a good DRY refactor - perhaps by extracting certain sections into a separate stateless component

* **Model validations** - if the ingredient grouping feature above is going to work, ingredient quantities must be integers (i.e. 0.5 rather than “one half”); there needs to be a way to validate that before a new recipe is saved to the database. Other validations could include making sure that all recipes have ingredients, usernames are unique, etc.

* **Recipe search** - A search tool could be useful - particularly one that renders matching recipes as the query is being typed (which I now know can totally be done with state and controlled forms!). I’ve also toyed with the idea of incorporating a third-party recipe API so users can search from a large collection of recipes available online and save certain recipes to their own “favorites” list - I think this could be really cool.

I’d also love to come back to my last project ([Bookable](http://codename-sara.com/bookable_rails_javascript_project)) and refactor it to add React and Redux - throughout the React/Redux portion of the curriculum, I kept seeing so many ways that Bookable could be improved by incorporating state (although I am grateful for the learning experience of building it “stateless” with JavaScript/jQuery/AJAX first)!

In closing: I’m quite proud of how this project turned out. I couldn’t even have imagined building something like this when I first started this program, and it is incredible to be able to look back now and see how much I’ve learned.  
og post goes here.
