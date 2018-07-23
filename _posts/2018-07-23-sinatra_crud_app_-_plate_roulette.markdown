---
layout: post
title:      "Sinatra CRUD app - Plate Roulette"
date:       2018-07-23 04:40:14 -0400
permalink:  sinatra_crud_app_-_plate_roulette
---


Project #2 is officially in the books!

**OVERVIEW**

For this project, I built a CRUD Sinatra application, featuring an MVC framework and RESTful routes, called Plate Roulette. The domain model is based on:

* Users, who **have many** Plates;
* Plates, which **belong to** a User and **have many** Ingredients; 
* Ingredients (Mains and Sides), which **have many** Plates

Users can choose from a list of main ingredients and side ingredients (or add their own), and Plate Roulette will randomly build a “plate” consisting of one main and two sides. Users can also create accounts and save, edit, and delete plates they have created.

As I learn more and add to my skillset, I want to come back and add in a few visual and/or stylistic elements. For now, though, I’m happy with how it turned out and that it functions as intended!

You can watch a video walkthrough [here](https://www.youtube.com/watch?v=z7KrniUYVsw). 

**WHAT I LEARNED**

* **Local Environment** - I experienced quite a few issues with the Learn IDE while working on my first project, so I decided to try working on a local environment (for the first time ever!) this time around. The setup process was easier than I thought it would be, and it worked out much better for me.
 
* **ActiveRecord/Sinatra** - I remember doubting whether or not the whole ORM/migrations/routes/ERB thing would ever “click” for me when I first started this module, but I GET IT NOW. Routes are basically a game of catch. ERB is like regular Ruby but with some “%” and “<“ and “=“ and “>” thrown in. Migrations change your database structure. ActiveRecord is like a bridge between your Ruby methods and your SQL database and gives you a bunch of helpful methods. 
 
* **I  ❤️ Ruby** - So elegant. So powerful. How can you not love it?
 
* **Debugging** - The process of debugging was exponentially smoother this time around. I’m not sure if it was because I had already gone through the process of building another project, or if it was ActiveRecord magic, but at no point did I get derailed or find myself “stuck” on an issue I wasn’t sure how to fix. This doesn’t mean that I never ran into issues - I had TONS of errors throughout the course of this project - but I was able to quickly find and resolve them when they came up. My debugging toolkit consisted of the following:

    * **Tux** - super handy for drilling down directly into the database for things you can’t do/see with Pry (for example, ```destroy_all``` for a given class) 
    
    * **Shotgun** - real time feedback is immensely helpful
    
    * **Pry** - both inline in my code and through the custom ```rake console``` command (which, btw, I’m not sure how I ever lived without and will be carrying on with me from this point forward)
    
* **Nested Form Structure** - I had to REALLY think through the structure of my nested forms in order to understand what a given params hash would yield. This took a bit of trial and error, and I even had to write out a hash “tree” to visualize the nested structure - but I got there in the end.

* **Seed data** - Although it wasn’t a requirement for this project, I knew I wanted to be able to see the app up and running right away so I could tell if everything was functioning as it should be - this meant I needed data in the database. I had never added seed data to anything before, but I noticed it was present in a few labs so I decided to take a swing at it, and it worked! It helped a TON to be able to populate the database right away (in some cases, right after I had cleared the database out) and make sure everything was as it should be.

There were also quite a few things (including a few mentioned above) that I was able to carry over from my experience building [my first project](http://codename-sara.com/gli_gem_knitpickr), including:

* Familiarity with Git and the terminal (and helped with the transition to a local environment as well)

* Frequent Git commits

* Debugging with Pry

* Not being afraid to break something because I know I can fix it

All in all, this was a very smooth process and I’m very happy with the end result. This is the closest yet I’ve felt to “real” web development! I’m so excited to keep going and can’t wait to see what Rails has to offer.

Check out Plate Roulette for yourself [here]( https://github.com/sarastanton/plate_roulette)! 
