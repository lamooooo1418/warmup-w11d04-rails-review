# Rails Review

For each of the following topics, please answer each of the questions. You can use links and images to support your answer. Once done please make a pull request.

## Has many Through

- [Rails Active Record Intro](https://github.com/sei-entropy/lesson-w11d02-rails-active-record#active-record-associations)
-[Hospital App](https://github.com/sei-entropy/hw-w11d02-rails-hospital)

### Questions

1. What is the role of a join table in a many-to-many relationship?
To Assosite the Two Tables together 
2. What two columns must be present in a join table?
present the two tables together using primary key of one of them 
as a foriegn key
3. Given the example below, edit the code to define a has many :through relationship.

    ```ruby
    class Customer < ActiveRecord::Base
     has_many :Product, dependent: :destroy
    end

    class Product < ActiveRecord::Base
    belongs_to :Customer
    end

    class Purchase < ActiveRecord::Base
    end
    ```



## Devise

- [Devise Lesson](https://github.com/sei-entropy/lesson-w11d03-rails-devise)

### Questions

1. What does the `current_user` method that the Devise gem provides?
Devise defines current_user as helper method so you can use it both in your controllers and templates. and represent the current user

2. What does the `authenticate_user!` method that the Devise gem provides?
The authenticate_user! class method (controller only), ensures a logged in user is available to all, or a specified set of controller actions. This method is invoked via a before_filter

1. Write a signout link using the `link_to` rails helper and a devise path.
   
   ```

  <%= link_to('Logout', destroy_user_session_path, method: :delete) %>        

    ```


2. How do I generate a devise model in the terminal?
rails generate devise MODEL

5. What are the trade offs for using a gem for authentication over a handrolled solution? (no real right answer)
Must Follow each steps also name convention but will Support security


## Validations

- [Validations Lesson](https://github.com/sei-entropy/lesson-w11d03-rails-model-validations)

### Questions

1. Which component, of Rails MVC, is responsible for the business logic?
Models

2. Assume the user's age is an optional field.  Write the validation to verify that a User's age is between 13 and 125 (inclusive).


3. What would `user.errors.messages` return (for the above User), if you assigned `user.age = 12`?


