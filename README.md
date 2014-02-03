---
  tags: git, todo, tutorial
---

# Git Todo

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

First, create a new directory in your home directory to contain your git repository:

```
cd ~
mkdir git-todo
cd git-todo
```

You should now be in a brand new directory. Run `pwd` to see that 
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
So, let's stage the changes you made as a precursor to actually
integrating the changes into the git repository.

```
git add README.md
```

Now, run `git status` again. You now see that there are "changes to be
committed". Great! Let's commit the changes. Once you do so, the new
README.md file will be in your git repository.

```
git commit -m "Initial commit."
```

The -m option to commit indicates that you are providing a message to go
along with this particular commit. Commits are the building blocks of a
git repository. When we think about a git repository, we think about it
in terms of commits and the relationships between commits.

## Using Github

So, now that you have a full-fledged git repository, let's introduce
Github to the mix. Github is an online service that augments the
experience of using git. 

Visit the following URL:

https://github.com/new

Enter the name of your repository, "git-todo". Select the "public"
option. **DO NOT** check the box that says "initialize this repository with a README".

Once you've done this, click "Create repository".

You will be taken to the git-todo repository page and be shown the view
for repository with no content. This is because our new Github
repository doesn't know about the commits on our computer yet!

You should see two sections on this page, one for "creating a new
repository on the command line" and one for "pushing an existing repository
from the command line".

We have an existing repository, so paste the 2 lines in that section in
to your terminal within the git-todo repository directory.

The first line that starts off with `git remote add` tells your git
repository where on the internet your Github repository lives.

The second line, `git push -u origin master`, instructs your git
repository to send it's commits to Github!

Once your `git push -u origin master` is successful, refresh the Github
page in your browser and you should see your "README.md" file. Congrats!
