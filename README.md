---
  tags: git, todo, tutorial
---

# Git Todo

## Instructions

Open up your terminal and follow along!

First, create a new directory to contain your git repository:

```
cd ~
mkdir git-todo
cd git-todo
```

You should now be in a brand new directory. Run `pwd` to see that 
your present working directory looks something like this:

`/Users/USERNAME/git-todo` (USERNAME is your operating system username)

Now, create an empty file in your current directory:

```
touch README.md
```

Great, now we have something to version control! 

Let's get started with git:

```
git init
```

This initializes the git repository. If you run `ls -a`, which list all
files in the current directory including hidden files, you should see
both README.md and directory called ".git". The dot preceding the
filename tells your operating system that it is a hidden file, which is
why we need the "-a" option for ls. Everything that makes your git
repository a git repository is in this directory! This means that if we
were to delete the .git directory.

Now we have to tell git which files we would like to keep track of.

Let's first run:

```
git status
```

This tells us that we have a file "not staged" for commit. In git, we
have to stage the files that we would like git to keep track of for us
because it's not always the case that we would like to keep track of all
the changes we just made. So, let's add the changes that we've made to
the repository with the following command:

```
git add README.md
```

Now, run `git status` again. We now see that there are "changes to be
committed". Great! Let's commit the changes. Once we do so, the new
README.md file will be in our git repository.

```
git commit -m "Initial commit."
```

The -m option to commit indicates that we are providing a message to go
along with this particular commit. Commits are the building blocks of a
git repository. When we think about a git repository, we think about it
in terms of commits and the relationships between commits.

So, now that we have a full-fledged git repository, let's introduce
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
