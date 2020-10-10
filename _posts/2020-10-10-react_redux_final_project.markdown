---
layout: post
title:      "React/Redux Final Project"
date:       2020-10-10 11:13:25 +0000
permalink:  react_redux_final_project
---


For my final project for the Flatiron School I decided to create a simple blog app. I will add functionality over time, but for right now it just allows a user to submit an essay with there name, title, content, and date. The essay can then be deleted. Their is a list of all essays and the can be read on a show page. 

For this project we were required to use React and Redux for the front-end. React is an open-sourced Javascript library(not a framework), maintained by Facebook. It is used for building user interfaces and UI components. Redux is another Javascript library used to mange state. For the back-end we were required to use Ruby as an API, which handles all of out data. 

**SETUP**

I used ['create-react-app'](https://reactjs.org/docs/create-a-new-react-app.html) to set up the front-end of the project. The will auto generate the basic layout, including src file with App.js and index.js, as well as some other files. It also creates a public file which holds the index.html file. There are also some image files that can be deleted for you no need them. This is what the tree will look like when you fire it up:


I used rails ['rails new my_api –api'](https://guides.rubyonrails.org/api_app.html) to spin up the back-end. The '-api' on the end of rails new tells the system that you need all the files in a rails app, except the view folder, because React will be handling all the front-end views. I used the the rails scaffold generator to spin up the models, controllers and database. Once that was finished I didn't really need to do much else. The one thing that did need adjusted, and I had this issue with my Javascript project, is that if you adjust to your table after generating it you will need to adjust your strong params for any form submission you make. 


**LAYOUT**

React makes use of components, which can manage their own state, and compose them to make complex UIs. We were required to use two container components and five presentational components. Container components handle data, and mange their own state. A presentational component is exactly what it sounds like, it just handles the presenting of data for the client. A good example of a container would be a form. Where as a good example of presentational would be the viewing on the data in the submitted form. 

We also had to use Redux and handle our state. React and Redux work very well together and even have the react-redux library to solidify their union. Redux makes use of the store, which holds the whole state tree. The only way to make changes to the store is by actions. We used Redux Thunk which is a middleware that allows you to call action creators that return a function instead of an action object. That function receives the store’s dispatch method, which is then used to dispatch regular synchronous actions inside the function’s body once the asynchronous operations have been completed.

I also spent some time with styling. Nothing crazy, but this was the first project where I really got to use CSS, and I also used react-bootstrap, which was really exciting(especially when it worked). 

**CONCLUSION**

This project was a stark contrast from my Javascript project. I really struggled with that one, to point where I didnt think I wanted to do front-end design, even though thats really wher emy pation lies. React really showed me that there are different ways to do things. It was really fun to create using React, and with Redux it almost becomes easy*. I look forward to working on front- end projects. I will also use this project to increase my skills. I plan to keep adding to this, and buidling it up to something I am completly proud of. 


*everything is relative





