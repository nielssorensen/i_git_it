What the git?
===
This is intended to be a quick and short introduction to git.  This assumes *some* knowledge of the Linux/Unix command line.  The lessons aim to amuse.  So if you are not laughing, or at least chuckling, there may be something wrong with you.

<h3>What is git?</h3>

git is a command line program and is "free and open source distributed version control system."
If any part of this is confusing, I highly recommend going directly to the [documentation](http://git-scm.com/doc) of git.


<h3>What is github?</h3>

Github is one of many websites that act as a "remote" for your repositories.

<h3>Why use git?</h3>
The answer to this question is probably just as important as understanding what it is.
People use git to track the changes made to a file.  Usually containing source code.
It allows multiple people to work on the same file. And they can be anywhere. 

<h3>A visualization of "stages" in a git workflow.</h3>

What happens when, where and why it’s important. It is intended as an overview rather than a cheat sheet.

```
============================================================================
----WORKING FILES----        ----STAGING----          ----REPOSITORY----

   NEW FILE
[ create file    ->          git add file             -> git commit -m ]


   UNTRACKED GIT FILE
    untracked    -> tracked(staged (to be committed)) -> committed


   TRACKED GIT FILE
[  unstaged file ->           staged                  -> git commit -m ]

============================================================================
```

Committed files are tracked files.
A file can not be committed unless it is tracked.

When a committed file is changed it is “modified” and in an ‘unstaged’
state.


If you don't find this simple diagram useful, perhaps "[The lifecycle of the status of your files](http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)" image will be more useful.
