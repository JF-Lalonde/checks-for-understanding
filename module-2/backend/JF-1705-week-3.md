## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

* Rails new app_name

2. What do Models generally inherit from in rails?

* ApplicationRecord

3. What do Controllers generally inherit from in a rails project?

* ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

* get "/show", to: horses#show

5. What rake task is useful when looking at routes, and what information does it give you?

* rake routes, it shows all the routes available from the routes.rb file.

6. What is an example of a route helper? When would you use them?

* A route helper is something like horses_path, which provides a linkable path to horses#index. They can be used to create links within views or controllers in an app.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

* `_url` provides the full url which is useful for linking to things outside of the app, and `_path` provides links to routes within the app.

8. What are strong params and why are the necessary?

* Strong params are a way for rails to limit what parameters are allowed to be modified inside an action in a controller. They are necessary to prevent an outside party from changing paramaters to give themselves admin access to an app.

9. What role does `form_for` play in helping us create our forms?

* `form_for` takes an argument of an instance variable and creates a create or edit form for a particular model.

10. How does `form_for` know where to submit the user's input?

* If `form_for` is dealing with an object that already has attributes filled out, then it knows that the form will be editing the entry. If the object has no attributes filled out then it knows the form will create a new object.

11. Create a form using a `form_for` helper to create a new `Horse`.

``` 
    <%= form_for @horse do |f| %>
      <%= f.label :breed %>
      <%= f.text_box :breed %>
      <%= f.submit %>
    <% end %> 
```
    
12. Why do we want to validate our models?

* We validate our models to ensure they are created with the attributes that we want them to have.
