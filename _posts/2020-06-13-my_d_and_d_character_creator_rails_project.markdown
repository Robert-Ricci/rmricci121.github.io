---
layout: post
title:      "My D&D Character Creator Rails Project"
date:       2020-06-13 18:50:12 +0000
permalink:  my_d_and_d_character_creator_rails_project
---


For my Ruby on Rails project, I decided to make a Dungeons and Dragons character creator. In the app you can create a user account. A user can create a character, and an adventure. An adventure is like a group of users that are playing together. From adventure you can create a campaign, which is the actual story that the characters are playing. Users view all adventures, and search for campigns by day of the week. I used MVC architecture to do this. 

For my set up I used rails generators. I decided not to use resource generator, but to instead to use model and controller seperatly. I've grown pretty comfortably with the syntax of them, where as resource I tend to get something wrong. I intend to practice with resouce to get better with it. I also made a point that when I needed to correct a table I didnt roll it back, but put a new migration, by the end I was pretty comfortable with that syntax, and reading the documentaton.

**MODELS**

I ended up going with for models, a user model, a character model, an adventrue model, and a campaign model. A user can create a character and an adventure. You can create a campaign with in an adventure with a characetr associated with it. This isn't exactly how I wanted to set it up, but how I needed to, so that I could meet the requirements. 

![](https://i.imgur.com/1DZHSFK.jpg)
![](https://i.imgur.com/GOnqdGH.jpgp://)
![](https://i.imgur.com/TOlivDM.jpg)
![](https://i.imgur.com/nwVEDq7.jpg)


I only did validations on a user and a character. I didn't think the other models required them. Each one has three validations, all of the user ones require presence and uniqueness for obvisious reasons, but the character only has uniqueness for name, because other players could play as that configuration of race and class. 

I added a scope method to the campaign model, so that a character could search for the day of the week they wanted to play. I'll be honest i fould this to be one of the harder concepts, of the requirements I had to meet. I had a really difficult time wraping my head around the idea, and I didnt feel like the documentation was decribing it well enough. With a little help from my Cohort lead, I was able to get it to work however. 

**DRY**

I tried to keep my views as light as possible. I used partials where I could. Both campaign and character have partials for new and edit. I also tried to keep my controller light, using helper methods when i could. I want to get better at that, but It will just take practice. 

**OMNIAUTH**

I decided to go with google for my Oauth, for no particure reason. I had some trouble with this in the beginning. I was having trouble deciphering the google documentation. I reread the lesson that we had, and was able to find a nice walk through on Medium, which really simplfied it for me. The only thing I wasnt able to get to work was the Google Signin button, on m view page, which is really frustrating. I decided not to waste too much time on it(only like an hour+), becasue it wasn't required. 

![](https://i.imgur.com/FgktDX1.jpg)

**CONCLUSION**

I had a lot of fun(and frustration) working on this project. It was nice to see how rails works. I was able to do alot of it on my own, and what I wasn't I was able to figure out either with google or our cohort lead, who was very supportive and accesible. The one thing that I'm not entirely happy with is my styling of this app. If I had another week, I could have gotton it to look more of how I wanted to, but I just ran out of time. I would like to get better at CSS, and html. So, I'm going to make that a prioity for our next project. 


