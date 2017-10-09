## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
  * Getting more comfortable with JS and getting back to writing algorithms was good, especially with the upcoming job search it was nice to rethink through the sorting suite.
2. What are some tools to help debug JavaScript code?
  * Console.log and debugger on the client side, pry js on the server side.
3. What are some tools you need in order to unit test your JavaScript?
  * Need mocha testing suite, and chai's assertions are also helpful
4. What is the syntax for invoking a function?
  * Parentheses after the function name, with or without arguments in them depending on if they're needed or not.
5. What's the difference between `==` and `===` in JavaScript?

 * Triple equals checks to see if the things being compared are exactly the same, including their data type. Double equals will do some type converting if needed when checking for equality.
6. What's the difference between asynchronous and synchronous JavaScript? 
  * JS is always synchronous, but using AJAX allows events to be added to a queue and be executed after the JS engine's execution stack is empty, which makes those events happen in an asynchronous order.
7. How do we setup a route when creating an API with Node and Express?
  * Haven't used Express yet so I'm not sure.
8. What do we use Knex for?
  * Knex is used to allow for SQL queries
9. What's `npm` and what do we use it for?
  * Npm is a package manager used to install various packages that we may want to use with Node.

#### Review  
10. What's the MVC design pattern? Describe each part of MVC?
  * Model-view-controller. The model interacts with the database via an ORM, the controller handles the "framework" of the ap, i.e. directing which routes will return which views and returning those proper views to the browser. The views are all the information to be displayed by the browser when the controller sends that particular view back to the client.
11. What is AJAX? What are some benefits of using AJAX?
  * AJAX allows for tasks to be delegated to event listeners and makes it possible for information to be processed without reloading a page.
12. What's a background worker? When would we want to use a background worker?
  * Background workers are processes that execute a task outside of the execution stack. After a page has loaded or code has been executed background workers will return information that can then be added. The idea of a background worker is for it to be given a task so that it can complete that task without "holding up" the rest of the code, and only after the main code has finished executing will it return its output.
