Rebase a branch
===
By now you get it, this lesson builds on the previous ones.
Same assumptions are made about the git workflow.


Round 4 - FIGHT!
---

So we've created a new branch and merged it back into master.
Now we're going to try something different.
Let's start with yet another new branch.

`git checkout -b poop`  
Did I catch you sleeping?
That's right, we can create a new branch AND check it out with the flag '-b' for the git command 'checkout'.

`git status`  
Shows we are on 'branch poop' just as expected.  
`git log --pretty=oneline --decorate`  
Shows that HEAD points to the last commit on all branches.
Including the remote ones.


`git rebase`  
`git revert`  
`git reset`
