## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

* At a high level, ActiveRecord is an ORM written in Ruby. It allows a web application, more specifically a model (if using MVC framework), to communicate with a database.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

* You could call #all, #save, #create, #new, #destroy, etc. These are all methods inherited from ActiveRecord.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

* Team.find(4). To find the owner, team = Team.find(4) then team.owner_id but without an association to the Owner table you couldn't directly find the owner belonging to that owner_id. You would need to manually create a method that would link team.owner_id = owner.id.

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

* Now you could just call team.owner on the team instance from question 3.

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

* It will be a many-to-many relationship. In both models there would be a has_many relationship to each other through the join table SudentsTeachers
* Diagram: http://ondras.zarovi.cz/sql/demo/ Load: "JF-week-2"

6. Define foreign key, primary key, and schema.

* Foreign key is an id in a table that corresponds to another table's primary key, thus establishing a relationship between the two. A primary key is an auto-incremented id in a table that is associated with the item in that id's row. 

7. Describe the relationship between a foreign key on one table and a primary key on another table.

* Using the example from question 5, the StudentsTeachers table has a foreign key of student_id and the Students table has a primary key of id.

8. What are the parts of an HTTP response?

* A code such as 404 or 200, a header, and a body (with or without content). 

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

* 1. #where, which returns an array of every instance that matches the argument.
* 2. #pluck, which returns an array of every attribute placed in the argument.
* 3. #group, which will group results from a previous method by an argument.
* 4. #create, will create an instance of a model inside your database.
* 5. #batch, will group into a batch of whatever size you pass it.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

* 1. rake db:create_migration NAME=whatever -- will create a migration file
* 2. rake db:migrate -- will run your migration files
* 3. rake db:create -- creates the database

3. What two columns does `t.timestamps null: false` create in our database?

* created_at and updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?

* Answered previously

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

* Answered previously

6. Give an example of when you might want to store information besides ids on a join table.

* If the relationship between both other tables has attributes in common, it could live on the join table.

7. Describe and diagram the relationship between patients and doctors.

* Doctors have many patients, patients have many doctors (if we're including specialists), so it's a many-to-many

8. Describe and diagram the relationship between museums and original_paintings.

* One-to-many, one museum has many original paintings.

9. What could you see in your code that would make you think you might want to create a partial?

* Repitition in your views, such as using a form more than once.
