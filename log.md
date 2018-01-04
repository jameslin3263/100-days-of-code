# 100 Days Of Code - Tailor Vijay - Log
My name is Tailor Vijay and I'm a digital nomad. I've taken the 100 Days of Code challenge on December 29th, 2017 and this is where I publish my daily progress. 

[Work Plan](https://github.com/tailorvj/100-days-of-code/blob/master/workplan.md) - It evolves on a daily basis, but basically rotates around React Web, Native and VR. 

I'm a media strategist, so I have a tendency to be very well planned and organized. I start slowly and pick up speed as I go, based on real progress.

[My Twitter updates](https://twitter.com/tailorvj)

01001010111010101001010100101001010010101001010100101011

## Day 5: January 3, 2018

### **Today's Progress**:

* None. 2nd late night work day this week. 

### **Thoughts**:

I must stop working so hard?! Phew

## Day 4: January 2, 2018 - Local and remote git branching and merging from the command line like a boss

### **Today's Progress**:

After a couple of sessions with sessions on https://try.github.io/levels/1/challenges/1 and using http://rogerdudler.github.io/git-guide/ as reference, I started branching and merging local and remote with confidence from the command line. 

Added the guide as a resource in my Trello board.

Just for the sake of good order, since this is the first time I've managed to do branching and merging from the git command line, here is the list of commands I used to publish this update on the Github repo:

```
$ git branch R1D4
$ git checkout R1D4
$ git commit -a -m "R1D4 log update"
$ git status
status said a file was created but not staged, so I staged it and committed again
$ git add images/20180102-codeacademy-progress.png
$ git commit -a -m "R1D4 log update. added missing image"
$ git push origin R1D4
$ git checkout master
$ git merge R1D4
$ git push origin master
```

Added .DS_Store to .gitignore

I think it's time for a little JS challenge :)

CodeAcademy has an [interactive basic JavaScript tutorial](https://www.codecademy.com/courses/learn-javascript-introduction/lessons/introduction-to-javascript/exercises/intro). Let's see what's going on there:

```
console.log('any string');
```

#### Data types

* Strings ('anything inside quotation marks, single or double')
* Numbers (any number, including floating point)
* Booleans
* null

I actually remember reading that in ES6 there are 5 data types. I'll look into it later. 

#### Math operators (for numbers)

1.	Add: +
2.	Subtract: -
3.	Multiply: *
4.	Divide: /

#### Built-in JavaScript objects

**String.prototype** (Instance required) properties and methods() [MDN String reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype):

* .toUpperCase()
* .startsWith()
* .length
* .trim()

**Math** (Library, no instance required) object methods() [MDN Math reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

* Math.random()
* Math.floor(x)
* Math.ceil(x)

**Number** (Library, no instance required) object methods() [MDN Number reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

* .isInteger(x)

```
// single line comment

/*
multi
line
comment
*/
```

### Thoughts

Interactive tutorials with good visual reference material to back it up while I work, combined with some Googling, seems to be the right combination for me. 

I've been pondering the creation of a flash card collection for memorization purposes, but daily practice is also great. Maybe I'll develop an app for that later. 

Anyhow, It feels good to go back to the basics. 

### **Link to work**: 

https://github.com/tailorvj/100-days-of-code/tree/R1D4

![CodeAcademy progress](images/20180102-codeacademy-progress.png)

## Day 3: January 1, 2018 - Happy New Year!!!

### **Today's Progress**:

* None. I was just working on a last minute project until I was done, which was way too late at night. The client was happy with the result though and I felt satisfied for actually making it in one go :) I hope this doesn't mean I'm going to be working late nights all year long though. 

### Thoughts

I'm going to have such days every now and then and there's nothing I can do about it. Work always comes first. I felt bad about it, but it's not like I was slacking or anything, just doing my job, which is fine. This gives me an opportunity to do double branch merging and pushing on R1D4

### **Link to work**: 

https://github.com/tailorvj/100-days-of-code/tree/R1D3


## Day 2: December 31, 2017 - Happy New Year!!!

### **Today's Progress**: 

* Organized my learning resources in a Trello board. 
* Found (after struggling with git command line. see below) this [interactive basic git command line tutorial by Github](https://try.github.io/levels/1/challenges/1) 

#### Cloned my 100DaysOfCode repo to my MacBook via Git command line (partial success) and Github GUI for Mac.
[Display git branch name (link to source)](https://coderwall.com/p/fasnya/add-git-branch-name-to-bash-prompt)

Add following lines to your ~/.bash_profile - **I don't think this has worked actually**.

```
parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
```

Clone the 100-days-of-code repo to my MacBook. Open terminal and type:
```
$ cd workspace
$ git clone git@github.com:tailorvj/100-days-of-code.git
```

This didn't work as is. I have to set my public key for this system to work with my github account. 

[Generating a SSH key from the terminal](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
```
$ ssh-keygen -t rsa -b 4096 -C "emailadderss@domain.com"
```
Saved it to the default file name then created a passphrase. 

**Add to ssh-agent**

- [x] Start the ssh-agent in the background

```
$ eval "$(ssh-agent -s)"
Agent pid 50505
```
- [x] automatically load keys into the ssh-agent and store passphrases in your keychain. edit `~/.ssh/config`

```
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```
 
- [x] Add your SSH private key to the ssh-agent and store your passphrase in the keychain.

```
$ ssh-add -K ~/.ssh/id_rsa
```
[Adding a new SSH key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

```
pbcopy < ~/.ssh/id_rsa.pub
```

Created a new SSH key in my Github settings, pasted the fingerprint and saved. - Yayy (Where is the AI that saves us from all that?). Anyway, I should be good to do my github cloning now. **YES, it workded!**

```
$ cd 100-days-of-code
$ ls
```

TODO: after branching, upload screenshot to repo, merge and use the image link here instead of the placeholder

![FAQ.md		images		r1-log.md	rules.md
README.md	log.md		resources.md	workplan.md](images/20171231-ls.png)

All the files are there indeed. I've already created a R1D2 branch, so now is the time to 

* switch to R1D2 branch 

Started following [Working with branches in Git](http://genomewiki.ucsc.edu/index.php/Working_with_branches_in_Git) wiki page.

```
$ git checkout R1D2
```

Stopped here and downloaded https://desktop.github.com/ 

I hope the following screenshots can portray how important visual feedback is when it comes to such complex processes:

![Github GUI Clone](images/20171231-github-gui-clone.png)

![Github GUI branch](images/20171231-github-gui-branch.png)

![Github GUI Added files](images/20171231-github-gui-added-files-to-branch.png) 

See my thoughts for today about this.

Next moves (not today):

* make my daily changes in the branch via command line git.
* create pull request.
* evaluate pull request.
* merge into master.

### Thoughts

I have to admit the concept of Git branching is pretty awesome, but it feels like git command line tool makes life hard for you in general and specifically when it comes to distinguishing exactly what you are working on and how to make the process of cloning from a remote repo, branching, then merging locally, then to the remote repo again, actually work. I will go into it again tomorrow maybe, but for now I'm going to make this commit via the Github GUI client.

After all of this struggle, I went into [#share-resources 100DaysOfCode slack channel](https://100xcode.slack.com/messages/C7F3MT7D2/search/git/) and searched for git. And voila! @ka11away to the rescue. Thanks buddy for the interactive git command line tutorials. 

![@ka11away to the rescue on #share-resources channel search results](images/20171231-ka11way-share-resources-screenshot.png)

I'm starting to see the added value of this documentation process. Collecting and organizing learning resources for this kind of learning process is time consuming. 

### **Link to work**: 

https://github.com/tailorvj/100-days-of-code/tree/R1D2

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

### **Link to work**: 

https://github.com/tailorvj/hello-world

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

### **Link to work**: 

none

