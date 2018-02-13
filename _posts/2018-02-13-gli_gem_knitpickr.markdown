---
layout: post
title:      "GLI Gem- Knitpickr"
date:       2018-02-13 00:47:02 -0500
permalink:  gli_gem_knitpickr
---


It feels incredible to be able to say that I have dreamed up, built, and published my very own Ruby CLI Gem! 

**OVERVIEW**

My project, titled “Knitpickr” *(all the trendy apps these days seem to end in “-r” - figured I’d join in)*, scrapes data from the Knitpicks website and allows users to browse yarn sold by Knitpicks. The user is first asked to choose their browsing method (browse by yarn weight, yarn fiber content, yarn name, or browse all yarn lines currently on sale), then is presented with a list of all yarn matching the selected browsing criteria. The user is then able to drill down and view specific details (such as name, fiber weight, fiber content, price, and sale status if the item is currently on sale) by selecting an item from the list.

You can watch a video walkthrough [here](https://youtu.be/yLOXyQu1E6w).

**WHAT I LEARNED**

* **Gems** 
    * I learned a ton about Ruby Gems - what they are (essentially a way to easily distribute code in the form of a self-contained library), how to build one (can be easily done with Bundler, which, ironically, is a Gem itself), and how to install and publish Gems on RubyGems.org . 
    

* **Git & Bash**
    * I confess to not having been in the habit of committing my work to Git very often prior to working on this project, aside from the ‘learn submit’ command used to submit labs in Learn. One of the requirements of this project was to commit early and often, so I had to become more familiar with Git and the command line. Part of this was figuring out how to add my working file to a remote repository on GitHub. Even working with RubyGems.org (installing, publishing, pushing out new versions, updating to a new version, etc.) required quite a bit of command line work, and I am much more comfortable with the command line as a result.


* **Scope of an entire project** 
    * Looking at an entire project from start to finish was an incredibly helpful experience. We often have blinders on when working through labs, only focusing on one particular objective at a time. Don’t get me wrong - I think is approach is very beneficial when learning as it lets you focus on just the specific thing you are trying to learn, but one of the dangers of this is that you don’t always know how all of the individual pieces fit together into a cohesive program. I had lots of “*ohhhh, so THAT’s why   *”  moments that really helped solidify my understanding of class methods vs. instance methods, how objects work together, which methods should go into which class, etc. **There’s nothing like working through a project from scratch to fill in the gaps in your knowledge.**


* **OO**
    * Related to my previous point, this project helped to solidify many object orientation concepts - particularly collaborating objects. Because I was defining my own classes, methods, and objects, I had to think about what it really means to be an object/class/instance in order to determine which one made the most sense to use. What classes did I need? What did I need those classes (and instances of those classes) to do? How did I need them all to work together?


* **Debugging** 
    * I also confess to not using Pry to debug at all before this project, relying instead on the error messages raised by Ruby and by the test suite when working through labs. With no test suite to rely on, I quickly realized I wouldn’t be getting anywhere fast without the ability to drop into a specific point in my code using Pry. Pry was also practically a necessity for sorting out my scraping selectors. I paid more attention to the error messages raised by Ruby as well - they are often immensely helpful on their own.


* **DON’T PANIC**
    * If I break it, I can fix it.


* **Googling is ok** 
    * Googling problems and asking for help is not only ok - these are necessary skills that I (and every programmer) will be using as a working developer. It isn’t “cheating.” The important thing is to understand the solutions you find and to be able to apply those solutions to your own particular issue.


* The rush you feel when you get something working for the first time is ADDICTIVE.


If you want to see it in action, [take Knitpickr for a spin](https://rubygems.org/gems/knitpickr) - I’d love to know what you think!
