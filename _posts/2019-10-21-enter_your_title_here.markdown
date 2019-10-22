---
layout: post
title:      "A Brief Overview of Bootstrap"
date:       2019-10-21 20:34:20 -0400
permalink:  enter_your_title_here
---


A  Brief Overview of BootstrapThis blog post will discuss the basic steps of setting up and using bootstrap with an app to achieve a more modern look.
For this example we are using 'Bootstrap as a Dependency.' This was easy to use.
Setting It Up
First, you want to use npm install bootstrap in the terminal to install the bootstrap dependency.
Second, you'll run npm install jquery popper.js in the terminal to install the jquery and popper.js dependencies. These are both needed to make Bootstrap javascript work.
Lastly, you'll want to use the following lines in your src/index.js file.

```
import 'bootstrap/dist/css/bootstrap.min.css';
import $ from 'jquery';
import Popper from 'popper.js';
import 'bootstrap/dist/js/bootstrap.bundle.min';
```

The above three steps import the Bootstrap javascript and css capabilities into your app, and now you're ready.
The example below I want to implement a drop down menu bar for my site navigation. The Bootstrap documentation makes it easy to add a button, this is the before:

```
<Link to='/signup'>Sign Up</Link>
<Link to='/find'>Find Gym</Link>
```

By using Bootstrap, I can change to the below, with dropdown capability:

```
<div class="dropdown"> 
  <a class="btn btn-secondary dropdown-toggle" href="#" role="button" id="dropdownMenuLink" data-     toggle="dropdown" aria-haspopup="true" aria-expanded="false"> 
  <i class="fas fa-bars"></i> 
  </a> 
	  <div class="dropdown-menu" aria-labelledby="dropdownMenuLink"> 
      <Link class="dropdown-item" to='/signup'>Sign Up</Link> 
      <Link class="dropdown-item" to='/find'>Find Gym</Link> 
    </div>
</div>
```

As you can see, by enclosing the Link tags within a 'dropdown-menu' div, and adding a button with a class 'btn btn-secondary dropdown-toggle', You can now enclose this code in a div class of 'dropdown'. Next you can use Bootstrap’s pre-set js and css to create a dropdown button.
If you were wondering what the popper.js was for, it is required for the above to work. You can use any font to display the bars icon for the dropdown button.
That’s all you need to have an interactive, streamline looking button to control your navigation.
Thanks for reading my blog, I hope you enjoyed it.
