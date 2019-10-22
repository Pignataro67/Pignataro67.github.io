---
layout: post
title:      "A Brief Review of JSON Serializers"
date:       2019-10-22 17:42:26 -0400
permalink:  a_brief_review_of_json_serializers
---


I am currently working on an app and I'm using json serializers. I figured I would write a post about it. Upon what I was researching I learned a lot and decided to highlight some concepts to help others in case they have similar issues. 

Ruby on Rails has a gem, ‘active_model_serializers’, which allows you to respond with JSON responses using Active Model Serializer. Everyone knows Rails uses 'magic' at times so set up looks like the below:

1) Add the gem 'active_model_serializers' to your Gemfile. 2) Run 'bundle install' to install the gem 3) Next, for each model in your application, run "rails g serializer 'model_name'". 4) Lastly set up your serializers to mimic your models. For example, if my model Users ‘has many goals’, then my Users serializer should be 'has many goals'.

But what if I want to include my goals association when viewing all Users, but I do not want to include my goals association when viewing just one User? I can specify the serializer in my render json statement. For example:

```
def show 
  @user = User.find_by(id: params[:id])
	render json: @user, :except => [:created_at, :updated_at], serializer: UserSerializer, status: 200 
end
```

In the UserSeralizer, I won't include the 'has many goals' association.

```
def index
  @users = User.all 
	render json: @users, :except => [:created_at, :updated_at], serializer: UsersSerializer, status: 200 
end
```

In my UsersSeralizer file, I will include the 'has many goals' association.

Thanks for reading my blog, I hope you enjoyed it!
