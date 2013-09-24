Create a repository on Github named git-todo

https://github.com/new

**Note: Don't forget that in all these commands, they are referring to my Github account, `aviflombaum`. That should be replaced by your github username. Remember your github username, it's part of your identity now.**

https://github.com/aviflombaum/git-todo

Open your terminal and follow the instructions below on how to setup your repository. We're going to `cd` into our home directory and make a new folder for our new repository.

```
cd ~
mkdir git-todo
cd git-todo

touch README.md
git init
git add README.md
git commit -m "first commit"
```

What just happened?

`git init` created a new repository in our git-todo directory. How? What did git init change in our file system? Try `ls -lah` to list all hidden files in that directory vs a non-git directory (you can just make a new directory in your home directory with `mkdir test-dir` and `cd` into that and then try `ls -lah`. The difference is what a git repository actually is.

`git add README.md` this informed git that there is a new file to start keeping track of. Git does not automatically keep track of everything in a directory, you must inform it of what you want to track.

`git commit -m "first commit"` this was what actually made a commit, a moment in time, an event, that git can now go back to whenever it wants. Think of it as taking a snapshot of the directory before and after that command and allowing you to reset the directory to those states.

Now look at your repository on github:
https://github.com/aviflombaum/git-todo

There are still now files there even though we just made a commit?

Why not? How do you fix that? What commands from the github setup of your repository did we not run and what do those commands do?

Run those commands.

**Note**

If you get an error about public-key-denied you have to setup your [SSH Key on Github](https://help.github.com/articles/generating-ssh-keys).

Now look at your repository on Github and make sure it has your README.md file.

https://github.com/aviflombaum/git-todo