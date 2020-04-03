---
layout: post
title:      "Sinatra MVC App Project "
date:       2020-04-02 20:43:13 -0400
permalink:  sinatra_mvc_app_project
---


For my second project, I made an app where a user can sign up for an account, log in, create "bookshelves", and then create "books" to put on them. It can be organized however the user likes, but I chose to make a bookshelf for each genre and put my books on their respective genre bookshelves. A user can also edit and delete both their books and their bookshelves, and log out of their account when finished. 

This project was really fun, but it was also a lot harder than I had expected it to be. There were a few things that helped me a lot though! The order that you make things really does matter. After setting up your gemfile, environment, rakefile, and config.ru, constructing your database is the best step to take. Adding each new table in your db file and migrating them means you now have the data you need, and can build the rest of the app off of it. I set up my application controller, before moving to models. Once setting up my models for each segment, I went ahead and made the controller and views for each one. I had three pieces to set up, the books, the bookshelves, and the users. Each book belonged to a bookshelf, and each bookshelf had many books and belonged to  user. 

One of my biggest problems is syntax errors. Something as small as a missing comma can keep your whole app from running, and if you change a word in one spot, you have to make sure to change it everywhere throughout your code. The search function in VS Code was very helpful for this, as I could find every instance of a word throughout my code and change the ones that were incorrect from there, rather than having to search through everything manually. 

All in all, this project was a good experience for me. With the support of my cohort lead and my peers, I was able to work thrugh each problem that arose, and ultimately created an app that I'm proud of. 
