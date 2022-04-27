# Learner’s Guide to Git and Github

### Part one: The basics of Contributing
###### By Janek Vedock

#### Forking a Repository
To contribute to a repository on github, you will need to fork it first, this will create a copy of the repository, under your name that can be merged back in at a later date with new changes


How to fork a repository

Go to the repository you want to fork




Click on the fork button in the top right corner

![fork-image](/docs/assets/git-github-1/git-github-1-1.png)

This will open your fork of the repository


Creating a Local Copy
While the code can be edited directly in the browser, this is a slow tedious process prone to error, by making a local copy on your computer, you can edit it with whatever software you chose and commit it to the remote repository
The easiest way to do this is by downloading the zip file from the code dropdown and unzipping it on your computer


Editing Your Files
While you can edit your files with whatever software you want, you will need some specific software to add your changes to github this software is git and can be installed from [here[(https://git-scm.com/downloads)
For this tutorial, we will be using the git command line but feel free to use the GUI if you wish
After you have changed your files, navigate to the main folder for the project, in this case /FTC-BASE-CODE
Once you are there right-click and select git bash here


 This will open a terminal window for you to type in
The first command you will want to type is 

```bash
git add .
```

which will stage all the new changes you have made.
The next command you will want to type is 
```bash
git commit -m “your commit message here"
```
this command will commit the changes to the git repository, replace your commit message here with a description of your changes, surrounded by quotation marks
With that, you have added your changes to your local git repository

Applying to your Fork
To apply your changes, you will need to authenticate git with github, so follow the instructions [here](https://docs.github.com/en/get-started/quickstart/set-up-git)

After that, to send all of your changes to your remote fork, you can use ```git push ```


To get the most recent changes to the remote on your machine you can use ```git pull```
Creating a Pull Request
Once you have pushed your pull request, you should be able to go onto the github page for your fork and see that your fork is ahead of the source (note: a branch can be ahead and behind at the same time)


To create a request to merge click on contribute, then open pull request


Finally click create pull request after reviewing your changes


After this it is out of your hands and someone marked as a contributor to the main repository can approve your changes, which will result in them being added to the main repository
