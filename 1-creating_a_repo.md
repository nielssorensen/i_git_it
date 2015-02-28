Creating a git repo
===
All the commands below should be typed out so you can commit them to memory.
They will also be annotated to explain what you see in your terminal.


Round 1 - FIGHT!
---
Let's make a directory and change (into that) directory.  
`mkdir dont_stop_git_it_git_it`  
`cd dont_stop_git_it_git_it`

So far we only have a new directory.
Let's initialize this repository and look at the status of it.  
`git init`  
`git status`  
Notice there is nothing to commit.  Let's change that and add a file.


`touch crap`  
`git status`  
Ok, now we have a new file.  Notice it is "untracked" by the repo.
Let's 'add' it to be "tracked."


`git add crap`  
`git status`  
Now we have a file but there is nothing in it yet. Let's add some text.

`echo "crap" >> crap`  
`git status`  
Oh crap, the file is listed TWICE!  What's happening?
Well, there is one that is ready to be committed but it has nothing in it.
How do we know?

`git diff crap`  
Aha, at the bottom of the output, we see the line '+crap'.
The plus sign prepended to the line means that it is new to the file.
But it's the same file, right?
It is, but let's check the "staged" version of the file.

`git diff --staged crap`  
Notice how the file ready to be committed has nothing in it.

We'll add the changed file to be staged and ready for a commit.  
`git add crap`  
`git status`  
`git log`  
Oh no! A "fatal" error? What'd I DO?! Don't worry, this is expected since there is no commit history. Yet.

Now for our first commit.
Always strive to make your commit message descriptive about the changes being committed.
(Here we're just having fun so it doesn't matter too much.)  
`git commit -m 'what the crap?!'`  
`git status`  
`git log --pretty=oneline --decorate`  
Oh god! What was that last command?! What did it DO?!
The log command shows you the git commit history.  And this is important.
Almost **THE** most important aspect of git.
There are four things we see here.  
1. The commit hash - Also known as a SHA1 hash and is unique to the repo.  
2. HEAD - This is a reference that denotes the next commit's "parent"  
3. master - This is the name of the default branch git creates.  
4. This should be the commit message we committed like, 'what the crap?!'  

Let's add some more text to the file!  
`echo "more crap" >> crap`  
`git status`  
`git diff`  
Alright, now we see this new line added to the file.
(Still prepended with the plus to denote that it is new to the file.)

`git add crap`  
`git status`  
`git diff --staged`  
This should be the same as the 'diff' above.
However, because we added it (staged it) we need to use the "staged" flag.

```git commit -m 'that`s a lotta crap!'```  
`git status`  
`git log --pretty=oneline --decorate`  
So, now we see two commits.  Again, it's the same structure.
This time however, we see that HEAD is pointing to the second commit.
Notice we are also still on the 'master' branch.

**You made it!**
On to lesson two.
