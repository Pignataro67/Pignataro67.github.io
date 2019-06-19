---
layout: post
title:      "Git Commands"
date:       2019-06-19 21:12:31 +0000
permalink:  git_commands
---


* Create a new directory locally in your terminal by typing the command-- mkdir <my-project> 
* Then switch to that directory by entering the command-- cd <my-project> in the terminal
* Initialize the directory by typing the command-- git init. You should only git init within the directory you want git to track

* Check the status of the repository by typing the command-- git status to see what changes have been made
* Create a README file by typing the command-- touch README.md within the directory
* Get a list of all the files in the directory by typing the command-- ls
 
* Add files to the git repository by typing the command-- git add <filename> or add all the files by typing the command-- git add .
* Commit the changes by typing the command-- git commit -m 'message about the commit'. Make sure the commit message is informative, specific, and in the present tense.

* Make a local copy of a repo from Github by typing the command-- git clone <URL>. Get the URL by going to the repository on Github and clicking the “Clone or download” green button. Use SSH as the URL type.
* See the names of each remote repository available by typing the command-- git remote. The remote repo you just cloned from is called origin
* Duplicate a repo by typing the command-- git fork. You will have your own copy and you can make updates. It's always good to complete/leave comments of what you did on anything you fork; Finish what you start!

* Connect the local repo to the Github repo by adding a new remote to a remote name by typing the command git remote add origin <URL>.  Push the local, committed work to the remote repo by typing the command-- git push -u origin master. Here origin is the repo name and master is the branch we are pushing to. The first time you push code up to the remote repo, use the -u flag but afterwards you only need to enter git push.
