---
layout: post
title:      "Password Security with Bcrypt"
date:       2019-08-28 19:40:15 +0000
permalink:  password_security_with_bcrypt
---

Password security is probably the most important aspect to a website. Activerecord has a macro, has_secure_password, that makes password encryption so easy it's almost magical. With just a few lines of code and installation of the gem, bcrypt, you'll have strong password security.

Bcrypt does the majority of the work maintaining password security. Bcrypt is an algorithm that takes user passwords and “hashes them,” converting them into strings of "utter nonsense" and adds a “salt” or small string of random data. The hashed passwords become incredibly difficult to revert to their original format. Hashed passwords are stored on the server-side in the password_digest column of a user table. Returning users’ password entries are then authenticated against the password_digest attribute.

has_secure_password lives in the user model and gives it three instance methods: authenticate, password=, and password_confirmation=. It validates that the password fields have been filled in on creation of a new account. Passwords are less than or equal to 72 bytes in size and it confirms that a user has entered the password correctly twice. If these conditions have not been met, a new account can not be created.

In a signup route, the has_secure_password validations are used. If a new user instance cannot be saved to the database with user input, the user will be redirected to a failure page. If a user instance can be saved to the database, its password will be hashed using the has_secure_password, password= method.

Given the user's input, the route will check and see if the user already has an account AND if they’ve entered the correct password. The password input is authenticated against the user instance’s password_digest attribute by calling user.authenticate(params[:password]), which will return false or the user object. When the aforementioned has occured, has_secure_password has done its job, and the user will now  be redirected to a success or a failure page.

In Summation, has_secure_password and bcrypt working together can offer great password security with only a few lines of code and the use of two methods: password= and authenticate.
