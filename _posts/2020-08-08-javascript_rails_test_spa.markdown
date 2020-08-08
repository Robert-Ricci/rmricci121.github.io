---
layout: post
title:      "Javascript/Rails Test SPA"
date:       2020-08-08 13:48:09 +0000
permalink:  javascript_rails_test_spa
---


For my Javascript frontend and Rails backend project I decided to do a single page assesment test application. The app would scroll through a series of questions, collect the answers into an array and save them to the database. Then a admin/user can view all the results and calculate the scores when needed. 

Backend:
I set the backend up first, since that was going to be the easier of the two. Like most things in Rails there is a shortcut for set up. 


`$ rails new my_api --api`

This sets everything up as if you just creates a new rails program, with the exception that it leaves the views out, because they will be handled by the Java	script frontend. Once you create the new API, you can use the rails generators, to get everything set up pretty quickly. I used the scaffold generator which will set up your model, controller, and migration.

`$ rails generate scaffold Post name:string title:string content:text `

You will still have to run. 

`$ rails db:migrate`

Frontend:
To get my frontend setup I first started with the files I would need. I will need one for all my javascript classes, plus one for main javascript, one for HTML, and one for CSS. 


To link the Javascript files to the main HTML, you have to use a script tag:

```
<script src="index.js"></script>
<script src="src/admin.js"></script>
<script src="src/question.js"></script>
<script src="src/test.js"></script>
```

Most of the work of the program is being handled with AJAX(Asynchronous JavaScript And XML). AJAX cycle is an event occurs, Javascript creates a XMLHttprequest, the object sends a request to the web server, the server processes the request, then sends back the response, Javascript reads the response, and an action is taken. 

I used the global fetch() method which comes form the Fetch API. With fetch() you are able to receive(GET) data:

```
function fetchAdmin () {
fetch(`${BASE_URL}/admins`)
.then(resp => resp.json())
.then(admins => {
for(const admin of admins){
let a = new Admin( admin.name, admin.username, admin.email)
a.renderAdmin();
console.log(a)
}
})
}
```

But also send(POST) data to a database

```
function testFormSubmission(){
event.preventDefault();
let name = document.getElementById("name").value
let selected = v
let test = {
name: name,
answer1: selected[0],
answer2: selected[1],
answer3: selected[2],
answer4: selected[3],
answer5: selected[4],
answer6: selected[5],
answer7: selected[6],
answer8: selected[7],
answer9: selected[8],
answer10: selected[9]
}
fetch(`${BASE_URL}/tests`, {
method: "POST",
headers: {
'Accept': 'application/json',
'Content-Type': 'application/json'
},
body: JSON.stringify(test)
})
.then(resp => resp.json())
.then(test => {
let t = new Test(test.name,test.answer1,test.answer2,test.answer3,test.answer4,test.answer5,test.answer6,test.answer7,test.answer8,test.answer9,test.answer10 )
console.log(t)
})
}
```
Conclusion:
I struggled alot with this project, and with Javascript in general. I found alot of the concepts confusing, but I was able to overcome them. It took a lot of help from my cohort lead, which I am super grateful for, and a lot of googling. I definitly feel like I'm grasping the concepts better than I was when I started this project, which gives me a sense of accomplishment. I plan on doing a lot oof reviewing during our break, so that I can hit it hard when we get back. 
