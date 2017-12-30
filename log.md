# 100 Days Of Code - Tailor Vijay - Log

## Day 1: December 30, 2017

### **Today's Progress**: Read Pro Git and did Github.com's hello-world tutorial

#### I've learned and implemented the basics of Git and Github

![Initializing the hello-world repo](images/20171230-github-hello-world.png)

The [Github hello-world tutorial](https://guides.github.com/activities/hello-world/) teaches you these basic concepts:
* Create an open source repository
* Start and manage a new branch
* Change a file and commit those changes to GitHub
* Open and merge a Pull Request

I've immediately implemented what I've learned on this repo by creating a [branch for R1D1 Log update](https://github.com/tailorvj/100-days-of-code/tree/R1D1) and merging it into master after I was done editing. 

Pro Git chapter 2 goes a lot deeper (and I have not finished the chapter yet):
##### Git basics
* Configure a repo
* Initialize
* Begin and stop tracking files
* Stage and commit changes
* Ignore certain files and file patterns
* Undo mistakes
* Browse project history
* View changes between commits
* Push and pull from remote repos

```
$ git init to start tracking changes in the current directory
$ git add *.c starts tracking all files with a .c extension in the current repo
$ git add README starts tracking changes to the README file in the current repo
$ got commit -m 'initial project version' commits changes in all tracked files to a version (called a commit)
$ git clone [url] clones the entire repo from URL including entire commit history to the local computer
$ git clone [url] foldername clones the project folder to a folder named foldername instead of the original folder name
```
Possible states of tracked files: unmodified ->modified then -> staged. There is a cycle here.
```
$ git status tells you in which state your files are, on which branch you are and if you have any untracked files.
$ git add filename/foldername to start tracking file filename or the entire folder foldername.
$ git add filename/pattern should be used to stage files for commit every time a change is made and you wish to preserve it on the next commit/snapshot
.gitignore file lists patterns for files to ignore.
Excercise: experiment with different glob patterns in .gitignore files in different fake repos.
$ git commit -m "commit message" commits staged changes into a snapshot
$ git -a -m "commit message" stages and commits all modified tracked files.
To add a last minute file to your recent commit
$ git add filename 
$ git commit --amend
$ git remote give you a list remote servers you are working with
$ git remote -v gives you their url's as well
$ git remote add remoteshortname URL adds a remote from URL and gives it the name remoteshortname.
$ git fetch remoteshortname gets all the different branches from the remote defined as remoteshortname
$ git push origin master pushes you latest commit on branch master to the server you originally cloned from (if you have write access)
```

### Thoughts

Github.com's tutorial has been a lot more effective in both time and effect. I've tried it hands on and immediately put into good use on this very repo. I should be looking for more resources like it and less resources like the Pro Git book, which is concise, but seems like an overkill and a time hog. 

MWeb Lite is a good Markdown editor for Mac OS X. I'm going to keep on using it to edit my MarkDown for theses updates. 

Updating takes a lot more time than it should. 

### **Link to work**: https://github.com/tailorvj/hello-world

## Day 0: December 29, 2017

### **Today's Progress**: Committing, Planning, Setting up shop

I’ve publicly committed to #100DaysOfCode on Twitter

Permalink: [https://twitter.com/tailorvj/status/946747480695128064](https://twitter.com/tailorvj/status/946747480695128064) 

![2017-12-29 100DaysOfCode committing tweet screenshot](images/20171229-100DaysOfCode-Committing-Tweet.png)

#### Markdown for the Github repo Log

I installed MWeb Lite app on my Macbook to be able to write MarkDown pages for the Github repo. Haven’t tested it yet, but it’s free, so I’ll look into it first, then make a decision about further steps. 

I’ve also installed a Google Drive script that converts Docs to Markdown and emails them to you. It’s been tested and looks very promising. I think it would be easiest for me to document my progress in a Google Doc, then convert it to MarkDown and publish on the Github repo. 

[https://github.com/mangini/gdocs2md](https://github.com/mangini/gdocs2md) 

### Thoughts

I can actually dive into this for hours unending, which is not what I’m trying to achieve here. This is a medium range project, so after initial push I’d like to stick to one hour a day. I’ve installed a pomodoro timer app on the Macbook to make sure I don’t go beyond the 1 hour limit. I’ll do 2x25 minute sessions every day, with a 5 minute break between them. 

Daily blogging will be done in the last 5 minutes of each day and if I feel like elaborating more about my experience, I may do a longer weekly recap blog post. 

My plan is to get back to the basics of web development and move up from there. First step: Git and Github. 

I have the kindle book Pro Git, which has a very thorough approach towards Git. Tomorrow I would like to read chapter 2 of it, but before I do that, I’m going to run through Github’s own Hello World hands-on tutorial

[https://guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/) 

### **Link to work**: none
