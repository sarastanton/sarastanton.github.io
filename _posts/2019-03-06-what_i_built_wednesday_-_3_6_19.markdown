---
layout: post
title:      "What I Built Wednesday - 3/6/19"
date:       2019-03-06 21:31:34 +0000
permalink:  what_i_built_wednesday_-_3_6_19
---


Hi Friends! 

Now that I've officially graduated from the Full Stack Web Developer program (*woo!*), I want to make sure my skills stay sharp - both in writing code and in writing *about* code. To that end, I've decided to try out a weekly blog segment called "**What I Built Wednesdays**", wherein I talk about what I've been working on over the past week. Exciting!

So - what have I been working on this week?

* **Portfolio** - Since I have a few networking events coming up soon, I wanted to make sure my [portfolio website](http://www.sarastantondev.com) was in tip-top shape and ready to be seen by new networking connections and potential employers. Most importantly, I deployed my last 3 projects (links are on my website - check them out!) and added them all to the 'portfolio' section of my website. I also *finally* set up my contact form, which may or may not have been broken this whole time (oops). I used Formspree for this - it took less than 2 minutes to set up, was free, and allows me to keep my website static (i.e. no back end needed), which opens up a lot of different options for hosting.  

* **Meal Planner** - I noticed soon after "finishing" (are any of our apps ever truly finished?) my final project, [Meal Planner](http://codename-sara.com/final_project), that the app breaks if a recipe saved to the current meal plan is deleted from the recipe database. Not good! This week, I went back in and fixed this so that a blank Recipe object (rather than 'null') is used, and the app no longer breaks in such cases.

* **Bookable** - [I wrote previously](http://codename-sara.com/ruby_on_rails_project_-_bookable) about the issues I had with implementing Goodreads OAuth after their recent HTTPS requirement (which none of the existing Ruby gems seemed to support). My workaround had been to manually edit an existing gem on my local machine, but I realized that this would not work with the deployed version. I ended up publishing a new gem based on an existing one (which was under the MIT license) to work with HTTPS, and I updated the [Rails + JavaScript version of Bookable](http://codename-sara.com/bookable_rails_javascript_project) to use the updated gem so that it was no longer necessary to manually edit a different gem. I'll get around to updating the pure Rails version of Bookable to use the new gem some time next week.

* **Calculator** - I also started a [new project](https://github.com/sarastanton/colorful-calculator) this week, and I'm super pumped! After working on a complex Rails/React project for the past few weeks, I'm going to shift focus and spend some time on a simple calculator using HTML, CSS, and vanilla JavaScript. JavaScript calculators are a fairly common tutorial project, but I'm adding a little twist to personalize it a bit (hint: color themes!). 

That's it for this week - I'll be back next Wednesday for another update!
