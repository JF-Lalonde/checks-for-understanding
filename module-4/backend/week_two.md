## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?
- ES6 uses arrow functions and ES5 doesn't

2. What's the difference between asynchronous and synchronous JavaScript? 
- Synchronous JavaScript happens within one thread and functions are handled one at a time. Asynchronous JS happens when tasks are sent outside of the engine to be processed in another thread by the browser, which can happen concurrently to the main stack being executed.

3. What are the four pillars of Object Oriented programming?
- Encapsulation, Abstraction, Polymorphism, Inheritance

4. What are some tools available in JavaScript to help you write object oriented code?
- ES6 allows for classes to be built using the constructor function

5. What are some key concepts to be aware of when refactoring your JavaScript?
- Try to encapsulate repetitive code into objects to be reused at multiple occasions. Break out code that is logically related into functions that you can call in multiple places without having to re-write it.

6. What's a callback function and what are some reasons when we use/need callback functions?
- Callback functions are functions passed as arguments into other functions. We can use these functions to take advantage of asynchronous JS and offload more demanding tasks to our page loads more quickly.

7. What's the scope of variables in Javascript?
- Variables declared outside a function are global, inside a function are local and only available to that function and any nested functions.

8. What's the difference between `==` and `===` in JavaScript?
- === doesn't perform a type conversion so values being compared must truly be equal to return true, whereas == converts the type so that values being compared don't need to be as strictly equal to return true.

9. Why do front end frameworks exist?
- These frameworks help organize and give structure to what would otherwise be an unstructured language. This helps clean up code and improve efficiency and reliability.

#### Review  

10. Why do people say "HTTP is stateless"?
- For example, unless some information is stored in cookies or sessions or some other way to store info, HTTP requests will not be associated to a user. 

11. Describe a RESTful API.
  - A convention that uses HTTP requests to interact with data with GET, PUT, POST and DELETE.

12. What are some main characteristics of a team following an agile workflow?
- Short, iterative cycles bringing the product to market ASAP and then working to improve on it.

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
- OAuth helps standardize login processes and allows users to use credentials from another appliaction. However if it's the only way to log in and a user doesn't have credentials from those other apps it could be disadvantageous.
