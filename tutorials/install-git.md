# The Git Version control system

## Introduction: Why bother? (optional reading)

There are many, many (many!) resources online that explain in great detail why one should use Git. Here I will give you only a quick explanation to motivate the need for this tool.

First, if you are either in a Computer Science (Informatik) or Electrical Engineering (Elektrotechnik) course *you will eventually have to to use Git*. For the EE students, the module PMSwEng in the third semester will require you to learn Git, for CS students it is introduced in the first semester. Nowadays Git has become the ubiquitous *de facto* Version Control System, to the extent that if you use something else, you're probably in the minority.

Okay then, what does actually Git do? Two things: It keeps the history of your files, and synchronizes them across two or more computers. How is this better than having multiple copies and using Google Drive or Dropbox?

Git has the advantages of *being able to solve conflicts*. If both you and your colleague change a file at the same time (or while one of the two is offline) a conflict will emerge, there are two *new* version of the same file. With Git this is not a problem thanks to a clever solution.

Under a more technical perspective, Git has other advantages as well. For example the history contains not only the changes of each file but also who did them, when they were made, a cryptographic hash of the data and more. Furthermore Git is decentralized, which means that any machine with Git (and SSH) installed can instantly become a server; Git does not need a central authority.

## Installation

You can download the official Git client at

  - https://git-scm.com/

If you happened to live in the 21st century, and not like command lines too much, *Sublime Merge* is a nice graphical front-end for git.

  - https://www.sublimemerge.com/

## Using git

![Magical incantations](https://imgs.xkcd.com/comics/git.png)

There is already a lot of very good material online, much better than what I could write here. If you don't mind videos, these are a few good resources to learn the theory behind the Git tool.

"I don't have time spend on learning the theory". Okay then, for the impatients out there:

  - Navigate to your project's directory with a terminal
  - `git init` creates a repository in your current working directory
  - `git add <file>` adds a file to the staging area
  - `git status` shows how things are going
  - `git commit` creates a "snapshot" of the files that you added to the staging area
  - `git remote add <remote name> <remote url>` adds a remote server
  - `git remote -v` shows you the remote(s) you've configured
  - `git push -u <remote name> master` uploads your commits to the remote
  - At this point, if it was too quick, you may have to look into the other resources below.
  - And maybe be more patient next time

If you want a very well structured explanation, watch the following 3 videos. Each is max. 30 minutes. You may want to try what you learned in each video before watching the next.

  - [Introduction to Git - Core Concepts](https://youtu.be/uR6G2v_WsRA)
  - [Introduction to Git - Branching and Merging](https://youtu.be/FyAAIHHClqI)
  - [Introduction to Git - Remotes](https://youtu.be/Gg4bLk8cGNo)

Note: if you learn everything from the videos above, you'll understand git better than most people.

If prefer an university lecture style, this recorded lecture from *The Missing Semester* at Cambridge University (ca. 1.30 hour) which is also good.

 - [Lecture 6: Version Control (git)](https://youtu.be/2sjqTHE0zok)
