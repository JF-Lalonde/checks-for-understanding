## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's your favorite project management tool?
  * Waffle. I like Pivotal Tracker too but I find Waffle to be more flexible which generally suits my needs better, and I find it easier to sync to GitHub.
  
2. Why do we create staging environments?
  * Staging is meant to exactly replicate the production environment (OS, database, etc.) so that we can ensure our code will work in production before we actually deploy it.
  
3. What are the characteristics of a good README (in your opinion)?
  * A good README contains everything a user would need to know to get the code running on their machine. The best READMEs may include screenshots of what to expect the app to look like, as well as links to give the reader more information when necessary.
  
4. What's one main improvement you're going to make to your code regarding accessibility issues?
  * Using semantic HTML tags when possible, as well as using the tabindex tag, will both help users using screenreaders. Using sans-seriff fonts with clear distinctions between font colors and background colors will also help visually impaired users.
  
5. What are some basic security concerns to be aware of when building applications?
  * Cross-site scripting, mass assignment, and SQL injection are some of the top concerns.
  
6. Why is continuous integration helpful/important?
  * CI allows for code to be merged frequently, which enables bugs or issues to be found and addressed more quickly.
  
7. What are some continuous integration tools?
  * HoundCI and TravisCI

#### Review  

8. What are some characteristics of "good" git workflow?
  * Logical branch names with commits that encompass logical units of work, descriptive commits and PRs, and never merging your own PR. When merging someone's PR, address any concerns or questions via comments on code lines as well as comments on the PRs themselves.
  
9. What are the four fundamental concepts of object oriented programming?
  * Encapsulation: the idea that data can be hidden inside of objects where it is inaccessible to unauthorized entities.
  * Abstraction: hiding the functionality of a method or function to a lower level that doesn't concern the user.
  * Polymorphism: the ability for a function to act on different data types
  * Inheritance: the concept of objects being able to have parent and children objects, and that an object is able to inherit functionality from parent objects, and impart functionality onto children objects.
  
10. What's a module in Ruby and what's the difference between a class and a module?
  * A module in Ruby is an object that can be included in a class to allow that class to inherit the module's properties. A module is different than a class because it holds no state, and therefore cannot be instantiated.
