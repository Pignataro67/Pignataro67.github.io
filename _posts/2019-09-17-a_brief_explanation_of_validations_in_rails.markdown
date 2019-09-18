---
layout: post
title:      "A Brief Explanation of Validations in Rails"
date:       2019-09-18 02:29:32 +0000
permalink:  a_brief_explanation_of_validations_in_rails
---


ActiveRecord provides Rails with built in methods that can help us make sure that our database ends up with data that is 'valid'. You may be asking yourself, "Why use ActiveRecord validations when many databases have validation features of their own?" The answer is because Rails doesn’t use them. Additionally, when you use ActiveRecord’s data validation, it will not matter what database you choose or may move to later because your validations will still be valid.For example, if we have a Users model and we set up a validation to ensure the user enters their name when creating a profile. It may look like this:

class User < ActiveRecord::Base
  validates :name, presence: true
end

We can see #validates takes in two arguments. First is :name as the attribute that we are going to validate and the second is a hash of options. In this case, we are making sure that the attribute can't be saved if it's empty. Let's look at something a little more complex. Let's set a validation  so the name can"t be duplicated AND has to be at least 8 characters longer. We can add in:

class User < ActiveRecord::Base
validates :name, presence: true
validates :name, length { minimum: 8 }
validates :name, uniqueness :true

Very cut and dry. The name must be present in the field when created, it has to be at least 8 characters long and there can't be another name exactly like it in the database.  Generally, it takes database activity to activate a validation, for example, if we used User.new then save after or User.create because create will  attempt to save it to the database. There is a way to validate without any attempt at writing it to the database and that is with the #valid? method. Let’s look at an example in our Users controller:

class UsersController < ApplicationController
def create 
  @user = User.new(user_params) 
	@user.admin = true if params[:user][:admin] == "true"
	  if @user.valid? && @user.save
	    session[:user_id] = @user.id 
	    redirect_to root_path 
	  else render :new 
	  end 
	end

Here we used a conditional to see if the new User we made is valid based on the validations we put in our User model. If truthy, it will save and execute the rest of the lines of code. Validations can help ensure only 'good' data is getting into your database. They also work in conjunction with error.messages that can be used to inform your potential user if a new user account can be created or not.

I hope you enjoyed my blog.
