
# Intro To MVC

## Overview

We'll discuss the structure of MVC web applications and explain the relationship between the different components in this application.

## Objectives

1. List the problems of creating a web application in one file
2. Define and describe the three components- models, views, and controllers- of the MVC framework
3. Explain the relationship between models, views, and controllers

## Model-View-Controller 

![MVC - Three Tier Application](https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/Overview_of_a_three-tier_application_vectorVersion.svg/593px-Overview_of_a_three-tier_application_vectorVersion.svg.png)

We could create a web application in one file, with thousands of lines of code in the same document. It would work. But it would also present us with some very big challenges. It would be close to impossible to debug our program, and our code would be virtually unreadable.

Instead, we use frameworks (Sinatra being one of them), to separate an application's code by function and make writing, reading, and debugging code a much more pleasant and simple experience.

The Model-View-Controller paradigm is a popular way of building frameworks for web applications - it provides a *separation of concerns* where groups of files have specific jobs and interact with each other in very defined ways. In a nutshell:

+ **Models:** With Rails\MVC Frameworks the models are part Logic Tier and Data Tier.  What this means is that the logical part of your app gets modeled after logic that finds data, creates it, manipulates it and saves it.  This is a separate concern and to separate a concern we use namespaces, in this case `ActiveRecord::Base`.  This is where the complex business logic of a user model goes.  There is usually little need to implement your own logic inside a model.  Models will behave better with this pattern and become more maintainable.  
+ **Views:** The 'front-end', user-facing part of a web application - this is the only part of the app that the user interacts with directly. Views generally consist of HTML, CSS, and Javascript.
+ **Controllers:** The go-between for models and views. The controller relays data from the browser to the application, and from the application to the browser.  Similar to an operator routing a phone call when telephones were analog.  Here are some further analogy's to bring more clarification.

## The Restaurant Analogy

If you've ever been to a restaurant, you'll know that there is a clear separation of concerns that takes place. The person cooking the food is not the same as the person delivering the food, and the person eating the food is someone completely different. Let's think of MVC as if it were a restaurant. 

### Models
First, there are the cooks (the models) that make the food. They take orders (from the waiter), and prepare the customer's meal. Once ready, they give it to the waiter to deliver to the customer.

In Sinatra, models are generally written as Ruby classes. Models can also connect to databases to persist data. Think of models as the main logic behind your web application.

### Views
The customers (views) place orders and receive food. The orders are placed with the waiter, who takes them back to the kitchen.

In Sinatra, views are written as `.erb` files, consisting of HTML and embedded Ruby (Ruby code written within html). They are what the user actually sees when they use your web application.

### Controllers
The waiters (controllers) shuttle between the kitchen and the front of the restaurant. They take requests from the customer to the kitchen, and take prepared meals from the kitchen to the customer. Without the waiter, our customers would be hungry and our chefs would have nothing to do.

In Sinatra, controllers are written in Ruby and consist of 'routes' that take requests sent from the browser ("GET this data", "POST that data"), run code based on those requests by using models, and then render the erb (view) files for the user to see.  


<p data-visibility='hidden'>View <a href='https://learn.co/lessons/sinatra-intro-to-mvc' title='Intro To MVC'>Intro To MVC</a> on Learn.co and start learning to code for free.</p>

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/sinatra-intro-to-mvc'>Intro to MVC</a> on Learn.co and start learning to code for free.</p>
