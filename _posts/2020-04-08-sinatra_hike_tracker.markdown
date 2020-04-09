---
layout: post
title:      "Sinatra Hike Tracker"
date:       2020-04-08 21:21:13 -0400
permalink:  sinatra_hike_tracker
---

We've recently had to create a content management system, using CRUD and MVC functionality. We could track anything important to us,so I decided to track all my hikes, as I been wanting a simple way to track them. The functionality is pretty simple, a person signs up, they are able to create a new hike. They can edit and delete their own ahikes. They can view other users hikes, but can't edit or delete them. 

To get started I used to the Corneal Gem(https://rubygems.org/gems/corneal) which is a Sinatra app generator.  So that set up most of the files and folders I would need to write the code for this program. To use Corneal all you need to do in you terminal is type:

1. `gem install corneal`
2. `corneal new APP-NAME`
3. Run `bundle`

After corneal sets up the scaffolding I had to go in a add the Models, Views, and Controllers I would need to create the code to make this app work. I also had to set up my databases. I went with two models, four views per model, and three controllers, one per model, one controller to rule them all, so to speak, and two tables for the two models. 

MODELS
The model is the 'logic' of a web application. This is where data is manipulated and/or saved. The two models I have are User and Hike. A user has many hikes, and a hike belongs to a user. I used ActiveRecord:

`has_many` and `belongs_to` for the functionality. 

Within the Models I also checked validations for username, email and password. 

	validates :username, presence: true , uniqueness: true
	validates :email, presence: true , uniqueness: true
	validates :password, presence: true 


For security I used

`has_secure_password`

Which works with the gem `bcrypt` to authenticate passwords. 

Views
This is the user-facing part of a web application or 'front-end' - this is the only part of the app that the user interacts with directly. Views generally consist of HTML, CSS, and Javascript. I created four views for the user and hike model. 

Users:	
1. Signup – Has a form that allows a user to signup for the sevice.
2. Login – Has a form that allows a user that has already signed up to login, 
3. Index – shows all the users that have created hikes. 
4. Show – shows a users own hikes.

Hikes:
1. Index – shows all the hikes that have been created.
2. New – allows a user to create a hike
3. Show – shows the details of a specific hike
4. Edit – Has a form that allows the user of a hike to modify it. 

Controllers
The controllers are the go-between for models and views. The controller relays data from the browser to the application, and from the application to the browser. I am using three different controllers. I went with three for a couple of different reasons. One reason was to make it easier to read, and second is for separation of concerns. Each controller has on focus, which should make it easier for someone else to come and look at your code and figure out where something is, if it needs changed. 

1. Application Controller – Is the main controller, that all the controllers work 
     from. It has all the requirements that you will need for any dependencies.   	
2. User Contoller – controls everything that has to deal with the user, views.
3. Hike Controller – controls everything that has to do with the hikes views.   

Datebase
This is where my data will be stored in the form of a table. it will keep my users data like username, email and password, and hike data like name, location, milage, and joined by. 


