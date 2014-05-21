---
  languages: bash
  tags: git, todo, tutorial
  resources: 4
---

# Git Todo

## Prerequisites

* [Follow the instructions from Github linked here for setting up an SSH key](https://help.github.com/articles/generating-ssh-keys)
    - Having an SSH key will allow you to communicate with Github using
      the SSH protocol. One of the benefits of this is that
      it will allow you to communicate securely with Github without
      having to type in your password.
    - You have successfully set up your SSH key to work with Github when
      running the `ssh -T git@github.com` command in your terminal returns:

      "Hi username! You've successfully authenticated, but GitHub does not
      provide shell access."

## Overview

This is a tutorial for creating the most basic git repository possible
and adding it to the online service Github.

Git is a "distibuted source control management system".

It is a "source control management system" in the sense that it helps
programmers to control and manage changes being made to a collection of
files and their contents. It is a critical tool for all software
development teams (even 1 person teams!).

It is "distributed" in the sense that many copies of a given repository
can exist, but each copy can operate independently of any other copies.
At the end of this tutorial, you will have 1 copy of your repository on
your computer and 1 copy of your repository on Github.

## Instructions

Open up your terminal and follow along!

## Create a file

First, create the directory "git-todo" in your home directory to contain your git repository:

```
cd ~
mkdir git-todo
cd git-todo
```

You should now be in the brand new git-todo directory. Run `pwd` to see that 
your present working directory looks something like this:

`/Users/USERNAME/git-todo` (USERNAME is your Mac OS X username)

Now, create an empty file in your current directory:

```
touch README.md
```

Great, now you have something to version control! 

Run the `ls` command to verify that README.md was created.

## Using git

Let's get started with git:

```
git init
```

This initializes the git repository, or in other words, it creates a
directory called ".git" which contains some stuff that git needs.

If you run `ls -a`, which lists all
files in the current directory including hidden files, you should see
both "README.md" and a directory called ".git". The dot preceding the
directory name tells your operating system that it is hidden, which is
why you gave the "-a" option to ls. Everything that makes your git
repository a git repository is in this directory! This means that if you
were to delete the ".git" directory then this directory would not longer
be a git repository.

Now you have to tell git which files you would like to keep track of.

Let's first run:

```
git status
```

This says you have a file "not staged" for commit. In git, you
have to stage the files that you want git to keep track of because it's not
always the case that you want to keep track of all the changes you just made.
So, let's stage the changes you would like to track as a precursor to actually
putting the changes into the git repository.

```
git add README.md
```

Now, run `git status` again. You now see that there are "changes to be
committed". Great! Let's commit the changes. Once you do so, the new
README.md file will be in your git repository.

```
git commit -m "Initial commit."
```

This command creates a new object in git called a "commit"
Commits are the building blocks of a git repository. They represent a set of
changes made to the contents of the repository. When we think about a git
repository, we think about it in terms of commits and the relationships
between commits.

The -m option to commit indicates that you are providing a message to go
along with this particular commit.

## Using Github

So, now that you have a full-fledged git repository, let's introduce
Github to the mix. Github is an online service that augments the
experience of using git. 

Visit the following URL:

https://github.com/new

Enter the name of your repository, "git-todo". Select the "public"
option. **DO NOT** check the box that says "initialize this repository with a README".

Once you've done this, click "Create repository".

You will be taken to the "git-todo" repository page and be shown the view
for a repository with no content. This is because our new Github
repository doesn't know about the commits on our computer yet!
It looks something like this:

![new github repository](http://flatiron-web-assets.s3.amazonaws.com/curriculum/git-todo/empty-github-repository.png)

We have an existing repository on our computer, so paste the 2 lines in that section in
to your terminal within the "git-todo" repository directory.

The first line that starts off with `git remote add` tells your git
repository where on the internet your Github repository lives.

The second line, `git push -u origin master`, instructs your git
repository to send it's commits to the Github repository!

Once your `git push -u origin master` is successful, refresh the Github
repository page in your browser and you should see your "README.md" file. Congrats!

Here's an example of what the repository will look like on Github with
the README.md file:

![github repository with readme file](http://flatiron-web-assets.s3.amazonaws.com/curriculum/git-todo/git-todo-github-with-readme.png)

## Resources
* [Pro Git](http://git-scm.com/book/) - [1.1 Getting Started - About Version Control](http://git-scm.com/book/en/Getting-Started-About-Version-Control), page 
* [Pro Git](http://git-scm.com/book/) - [2.1 Git Basics - Getting a Git Repository](http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository)
* [Pro Git](http://git-scm.com/book/) - [2.2 Git Basics - Recording Changes to the Repository](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository)
* [LearnGitBranching](http://pcottle.github.io/learnGitBranching/) - [Introduction Sequence: Introduction to Git Commits](http://pcottle.github.io/learnGitBranching/), page NA
