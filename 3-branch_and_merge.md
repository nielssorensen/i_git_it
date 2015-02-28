Branch and Merge
===
This lesson builds on the last.
The git workflow in this lesson assumes you are not working on another repo.

Round 3 - FIGHT!
---

Let's create a new branch to do work in.
In general, it is always best to do work in a branch named after a feature you may be working on.  
`git branch pee`  
`git status`  
`git log --pretty=oneline --decorate`  
Hmm, interesting.  Seems like that did nothing.  How can we check?

`git branch -a`  
AHA! Now we see the branch that we made.
But we are still on branch master.
How do we get to the new branch we made?

This is how.  
`git checkout pee`  
Now we have a message that we changed branches.

`git status`  
`git log --pretty=oneline --decorate`  
Huh, same info as when we were in the master branch.

`touch pee`
`git add pee`  
`git status`  
`git log --pretty=oneline --decorate`  
So far, the history is the same as master.
Now we're going to make the branch histories start to diverge.

```git commit -m 'pee!?!?!?!' pee```  
`git status`  
`git log --pretty=oneline --decorate`  
WHOA! This looks weird. What am I looking at?
The topmost commit is the most recent.
It shows HEAD pointing refering to the most recent commit on branch 'pee'.
But I see another HEAD in the commit history.  
Yep, that's pointing to the latest commit on the master branch.
Which is on origin. Which, in this case, is Github.

Pay close attention here.
This history **ONLY** exists in this branch.
That means that the pee file only exists in this branch too.
How can we check?

Let's change back to the master branch.  
`git checkout master`  
`ls`  
Notice here we only see the crap file.

Let's do some more sluething.  
`git status`  
Ok, that was expected.  
`git log --pretty=oneline --decorate`  
Hmm, only the original two commits.
Interesting.

So now, let's merge the pee branch's history INTO the master branch.  
`git merge pee`  
"Updating"  
Ok, one file changed.

Let's take a closer look at what just happened.  
`git status`  
Hmm, "branch is ahead of 'origin/master' by 1 commit."
This is because of the new history we merged in from the pee branch.

Let's look some more.  
`ls`  
There is the pee file.  
`git log --pretty=oneline --decorate`  
Here is that new commit from the pee branch.

Take note!
Locally, HEAD now points to this third and latest commit for both branches.
However, on origin, HEAD still points to the second commit.
Let's fix this.  
`git push origin master`  
`git status`  
Ok, nothing to see here, moving on.  
`git log --pretty=oneline --decorate`  
Awesome, now both remote and local HEAD reference the same topmost commit.
Local branches master and pee also have HEAD pointing to the last commit.

FINITO!
