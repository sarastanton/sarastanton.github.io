---
layout: post
title:      "Ruby on Rails project - Bookable"
date:       2018-09-26 09:44:50 +0000
permalink:  ruby_on_rails_project_-_bookable
---


I built a Ruby on Rails app!

**OVERVIEW**

Bookable is a Ruby on Rails application that lets users view and contribute to a list of books (including author, genre, and page count) available to all users, and add books from this index to their own personal "My Books" list. Users can mark books as "read" or "unread," track the total number of pages they have read, and leave ratings and reviews that are visible to all users. Users can also create an account through a traditional signup form, or sign in with an existing Goodreads account.

The domain model is based on: 

* Books, which **belong to** an Author and a Genre;
* Authors and Genres, which **have many** Books;
* Ratings and Reviews, which **belong to** a User and a Book; and
* ReadStatuses, which **belong to** a User and a Book and function as a **join table** between the two (Books **have many** Users **through** ReadStatuses, and Users **have many** Books **through** ReadStatuses)

Right off the bat, I had an interesting challenge in trying to figure out how different Users could track their “read status” (i.e. read or unread) on the same Book. It wouldn’t work to have a “read/unread" attribute of a specific instance of a Book because the value of the attribute for that particular Book instance would have to be different for different Users. I decided to create a join table called “ReadStatus” that could have a new instance per Book and per User.

Routes for Reviews and Ratings are nested under Books because it would not ever make sense to have a Review or Rating that was not associated with a specific Book. Reviews and Ratings cannot exist on their own without a Book (or without a User, for that matter).

You can watch a video walkthrough [here](https://youtu.be/hg4sW2svfkA).


**WHAT I LEARNED**

* **OmniAuth** - It was quite challenging to get OmniAuth working with a Goodreads strategy. I could have used a different provider (such as Google, Twitter, GitHub, etc.), but I was determined to find some way to get the Goodreads strategy working because it made the most sense for my domain model. To make a long story short, I found two things: (1) an OmniAuth Goodreads strategy gem that was outdated and no longer working, and (2) a GitHub repository with updated working code for a Goodreads strategy that was non-gemified. After a few days of dead ends, I learned that it is possible to edit your local copy of a particular gem, and was able to update the outdated gem with the non-gemified updated code to end up with a working OmniAuth strategy. 

* **Tests** - One of the goals I carried over from my [last project](http://codename-sara.com/sinatra_crud_app_-_plate_roulette) was to write a few tests for my project. I did end up writing a couple of tests this time around (both model and feature tests) using RSpec and Capybara…although, admittedly, *after* I had written my code and had the app up and running. For my next project, I will aim to write at least a couple of tests *while* I write my code in order to practice test-driven development.

* **Styling** - Another goal I set for myself on this project was to incorporate some styling. The result here - navbar, background color, color change on hover, tables, etc. - is nothing fancy, but definitely nicer than plain black text on a plain white background. I used Bootstrap, but in hindsight I would probably have been better off just sticking with plain CSS as I ended up overriding most of the Bootstrap styling with custom CSS anyway. Adding styling to this project taught me that (1) my CSS skills are quite rusty, and (2) I am so excited to see what I can do once I get into JavaScript + Rails in the upcoming curriculum modules!

* **Rails!** - Rails is POWERFUL. Form helpers, routes, and generators all do heavy lifting, but it's essential to understand what they are doing in order to be able to get them to do what you want them to do. Building a foundation with Sinatra helped a lot in this regard. Working with something so well known and used professionally felt like reaching a milestone. To be fair, Ruby CLI apps and Sinatra are also used professionally...but are not as widespread as Rails.

* **Refactoring** - This was possibly the first time I have ever taken refactoring seriously. I made use of partials whenever I could, and reaped the benefits when I decided to make some changes in a particular form - instead of having to change code in multiple places (ex: the "new" form and the "edit" form), I only had to change it once in the partial. Beautiful! I also took the time to go back through the entire project after everything was working properly to make sure everything was as lean and DRY as possible, through the use of helpers -  this made my code much more readable, which helped zero in on issues faster because there was less code to read through. 

Things I carried over from my [last project](http://codename-sara.com/sinatra_crud_app_-_plate_roulette):

* **Seed data** - Taking the time to write up some seed data was very helpful again this time around - particularly in cases when you need to drop your database. Running “rake db:seed” to reload seed data is exponentially easier than having to recreate saved database items one at a time in the console or through a form!

* **Nested forms** - I often tripped over myself trying to conceptualize nested forms in Sinatra, but the power of Rails (specifically route helpers, URL helpers, and form helpers ) made this a breeze this time around.

* **Debugging** - I have a pretty effective debugging workflow down at this point. The built-in Rails console was incredibly helpful as a way to test out methods and see what my object classes were doing. Pry was also a mainstay again, helping to see what is going on "under the hood" of the application at any given point.

* **I still ❤️Ruby**  and you’ll never convince me otherwise.

* **ActiveRecord** - I became even more familiar with the various ActiveRecord methods I have learned, and learned a few new things (like class-level ActiveRecord scope methods and ```build```) as well.

Over these past few projects, it has been incredible to think up an application and watch it come together into a functioning product. I pushed myself to be a bit more ambitious with this project (styling, tests, refactoring for lean controllers/views and DRY code, etc.), and I am proud of how it turned out.

Check out Bookable for yourself [here](https://github.com/sarastanton/bookable)!
