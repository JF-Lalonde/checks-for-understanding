## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
  * Node is a backend runtime environment for JavaScript built using Chrome's V8 engine.
  
2. What is Express? What is Express similar to in the Ruby world?
  * Express is a web framework for JavaScript. Express would be similar to Rails except Rails is much larger and more opinionated. Express would be closer to Sinatra but Sinatra is a DSL not a web framework. So I guess Express is most similar to Padrino.

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
  * Verb, then path, then ideally a controller method. Something like `app.get('/home', homeController.getAllData)`
  
4. What do we use Knex for?
  * Knex is a SQL query builder for JavaScript. It allows us to query our database to return relevant information.
  
5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?
  * Using Express we limited database queries to the model layer, building functions that would then be called by the controller, which would in turn serialize the information for the views. The routes also lived in a separate layer, only calling on controller methods. So the MVC pattern was similar to a Rails app, expect that we didn't have a separte views layer.
  
6. How do you execute raw SQL in node?
  * By using knex, we have access to knex.raw() which takes raw SQL queries.
  
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
  * Advantages are that both apps can be built using different languages/libraries/frameworks and can be updated/refactored at different times. Disadvantages are that both ends need to be formated more carefully to ensure they can communicate information properly.

#### Review  

8. Describe DNS.
  * Domain-name Servers host a list of the corresponding IP addresses for domain names. They return a website's IP address to the browser after receiving a specific domain name.
  
9. What does writing clean code mean to you?
  * Writing clean code to me means that someone else (or me, later) can look at the code and see what its purpose is easily, all the while being DRY and following conventions for the language/framework.
  
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?
  * Probably would need a hotel room class responsible for what a room contains (e.g. beds, amenities, etc.), a user class with multitenancy to account for administrators, guests, staff, etc. If a hotel was large enough the beds could also have their own class and be responsible for their size and whether or not they were clean. A hotel would also likely have a kitchen, which would be its own class and have a chef class, sous-chef class, busboy class, etc. that would inherit from it.
