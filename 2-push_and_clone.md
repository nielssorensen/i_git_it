Pushing and cloning a repo
===
We are going to use github for this lesson.
This assumes you already have an account **AND** completed lesson one.

Round 2 - FIGHT!
---
Go ahead and open a web browser to github.
From your account,  create a new repository.
Because we've already made a repo, all we need to do now is add the remote.
Back to the terminal!

`git remote add origin` YOUR_REPO  
`git remote -v`  
Now you should see two lines, one for 'fetch' and one for 'push'. 
Both with the name 'origin' as we specified when we added the remote.

Now, let's push our master branch to origin.  
`git push -u origin master`  
If done correctly, there will be 8 lines.  
The last line should look something like this:  
'Branch master set up to track remote branch master from origin.'

Now let's do something dangerous.
Let's delete our local branch.  Yikes!  
`cd ..`  
`rm -rf dont_stop_git_it_git_it`  
Oh god, my stomach just turned.  Where did that directory go?

Let's get that repo back.  
`git clone` YOUR_REPO  
`cd YOUR_REPO`

Now let's take a look at the repo.  
`git status`  
`git log`  
*PHEW!* Awesome! Everything is still there and the history is safe.
It should reflect the same exact history before you removed the directory.

All done! Ready for the next lesson?