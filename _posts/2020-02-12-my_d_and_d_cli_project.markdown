---
layout: post
title:      "My D&D CLI Project"
date:       2020-02-12 12:37:29 -0500
permalink:  my_d_and_d_cli_project
---



![](http:/www.doubledanegames.com/wp-content/uploads/2017/10/dungeons-dragons.png)  
I'm going to talk about my first Ruby Gem. I'm going to go over the requirements. I will also discuss my planning and how I attacked the project. I knew I was going to want to setup my local environment to work on this project, and Flatiron had a great step-by-step walk through. So once I had that done, I moved on to the actual project. 

The first thing I did was go through all the requirements to pass the project:

* Your CLI application must provide access to data from a web page.
 
* The data provided must go at least one level deep. A "level" is where a user can make a choice and then get detailed information about their choice. 
 
* Your CLI application should not be too similar to the Ruby final projects.
 
* Use good OO design patterns. You should be creating a collection of objects, not hashes, to store your data.


Once I figured out what I needed to do for the project, I went through and watched all the support videos. Not just the ones by Avi, but out Cohort Lead Annabel, had made a few that helped as well. Especially with setting up my Github repository. We had been prompted prior to starting the project to figure out what we wanted our project to do, and I decided to make a mini Dungeons and Dragons character finder. The app would allow you to list the different races and classes, you can then make a selection and it will give you basic info about each one. It would allow you to exit the app and got back and forth between the race and class list. 

I knew using an API would be easier for this because of how much info there would be to parse. Luckily, but not necessarily surprisingly, I was able to find a good one, that had all the information, in neat little arrays and hashes. I used the Ruby gem 'HTTParty' to get the data from the API. I installed the Ruby gem 'Pry' for debugging purposes, as well as the Colorize Gem to add a little pop of color on some of the puts lines.  I ended up setting up four different classes for this project. 

* An API class – which was responsible for retrieving the data. 
* A Race class – which handled the information of character race.
* A Klass class – which handled the information of character class. It spelled with a 'K' as not   
 to get it confused with the 'class' keyword'.  
* A Controller class – this class handled all of the interface. Any input taken or info printed or 
puts to the screen happened in this class. 

Over all this project was a great test of everything we had learned up until now. It wasn't easy, I had to change my approach at least once. Our cohort lead was a great help, what with the twice a day office hours. She even took the time to have a one on one, when I was having particular trouble with create a method for when an invalid entry was entered. I really enjoyed working on this project. 

I'm looking forward to what comes next. 


