---
layout: post
title:      "A Brief Review of APIs"
date:       2019-08-14 19:44:08 +0000
permalink:  a_brief_review_of_apis
---


Some acronyms are difficult for me to remember and API is one of them, but I digress. API stands for Application Programming Interface. What it does is it allows communication between two Programs in a common language. For a side project I am working on called Lyber, I am using two different APIs, one for route mapping and one for OmniAuth github logins.

APIs are essentially a list of commands, for example, when I have a user login through Github. What happens is Github  executes a bunch of commands and sends something back via the api, usually in the form of data. When a user logs into my website with Github, Github then sends a hash, or object, of data that you can then use to extract data. APIs can be though of as a pattern of requests and responses.

With Lyber, the user does not see the Lyber website and most users will more than likely never know they are interfacing with Lyber when they try to login. APIs allow you to use the functionality of another program without your user’s ever having to leave your app or website. This is great because big names like Google, Github, etc. "assume" the security risk and are less likely to have data hacked because they have better password securities to protect your user's information.

API Keys are like very long passwords. They are a value assigned by the service that provides the API.  My app Lyber, combined with Github, identifies my application and requests.  When you call the API in your program, your API key will be part of the request. This will enable the service to identify your app. Next it will accept or reject your request based on the validity of your API key. Lastly it will send back the requested data or an error if the key is invalid.

API Keys, especially from Google, Facebook or Github will provide a higher level of identification and authorization; a higher level than you could create yourself. I keep them in a "secret place", for example, my gitignore file.

APIs are a great way to add higher level security functionality to your app or website. I hope you enjoyed my brief review of APIs!
