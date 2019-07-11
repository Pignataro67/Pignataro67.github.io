---
layout: post
title:      "A Quick Explanation of git and github"
date:       2019-07-11 20:51:48 +0000
permalink:  a_quick_explanation_of_git_and_github
---


Upon starting the Flatiron online program, I found using Git and GitHub confusing at times. It certainly did not help that the names of both are similar. So I asked myself what are they and why do we need to use them?  I soon discovered using both Git and GitHub is a must for any career in programming because of version control. Version control allows you to integrate and record the coding changes from other collaborators. This is important because employers want employees who understand this concept, and version control skills allow you to contribute to work and projects. Also, version control helps you connect with the programming community. Version control is intertwined with Git and GitHub.

Let me explain what Git and GitHub are. Git is a version control tool that provides all of the basic functionality. GitHub is a platform derived from Git and gives you and your team the necessary organization for tracking and reviewing, among other things, your projects. Now I'd like to run through a hypothetical issue and how Git and GitHub would be used.

**Workflow overview**
In the workflow of a project, it begins with an issue tracker. Think of an issue tracker as a problem ticket that can be looked at by a programmer. An issue can be buggy code or a new feature that would help the functionality of an app. A contributor to a project can have any or multiple issues to address. When you work on the issues, you create a new branch.

Branches compartmentalize your project and make them organized. The master branch holds the living version of your project. When you branch from the master, which allows any contributor to make and test their changes independently of the master. Once they are satisfied with the changes, they can combine or merge them into the master.

While working on the project, you’ll be making commits. A commit keeps records of changes you make on the branch. It shows the timeline of workflow changes. Commits are great because they can be viewed by other collaborators on your team. Pull requests are important to the workflow of the project. A pull request is a request to have the branch you’re working on integrated with the master branch. Once the pull request is integrated or merged, it’s now part of the project. Pull requests show whoever is conducting the pull requests what changes have been made against the master branch.

**Operation**
Once you’re ready to start working on a project, you must Fork from the repository’s page on GitHub. Forking the repo page creates a copy, which will allow you to work on it. Once the repo is forked, you’ll have to Clone it and copy the URL. Now from Git, you’ll have to do a few steps in order to work on it. Within Git, you’ll have to navigate to the correct directory where you’ll keep your copy. This is done by typing 'cd' along with the filepath name, for example, 'cd filepath'. Then type git clone along with the URL you copied (i.e. - git clone URL). This will download all the info you forked and cloned from GitHub.

After you’ve finished your work, its time to save the changes to the master branch. This work will be done in Git. Within Git, you’ll type git status which shows the changes that have been made to the branch you’ve worked on. They show up in red font. After this step, type git add -A. This command is necessary as it commits the changes made to the file. The next step is to commit the change and add any messages about the change. Typing git commit -m and then in quotes adding your commit message, for example, git commit -m “'commit message'”. The message should be in present tense and concisely describe the change. This message will show up on the GitHub repo page, so it’ll be helpful to other contributors. The final step is to upload these changes to the master branch and GitHub. Typing 'git push' tells git to send the changes to the original repo master branch.

Verifying the changes can be done within GitHub. Click the compare and pull request tab. If you don’t see this notification, just click ‘New pull request’, then select the development branch on the pull request screen. Here we can fill out our pull request description and submit it for review. It’s very common that you might have to make additional changes to the project. All of these steps are repeated for each change. I hope this helped to explain Git and GitHub.


