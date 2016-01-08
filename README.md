# about-git


Hello, I wrote an quick fact sheet for git users before. Here is the part that could be useful to us.

## What is special in git

"stage" (git add ), "commit" (git commit ) and "push" (git push) are the three steps. "stage" is like a dry run and tells git what to commit.
So here are the commands:
git add .
git commit -m "your message."
git push
## FAQ

P: **I am too lasy to type in `git add .`.**

S: The magic potion is `git commit -a` which will do the staging and commit at the same time.

P: **What has been changed since last stage?**

S: `git diff` shows that.

P: **I typed in the wrong commit message.**

S: `git commit --amend` will allow you to change the commit message you typed in before.

P: **I forgot to put add some files.**

S: Just add the file and use `git commit --amend`. This will allow you to replace the previous commit.

P: **I accidentally added a file to staging.**

S: Should unstage the file. `git reset HEAD filename.md` will do.

P: **I want to discard the changes I made since last commit.**

S: **This can be dangerous.** `git checkout -- filename.md` can revert averything back to the last commit. But it discards all the changes and can not be recovered. DO NOT USE IT.

P: **I need to check what has changed in every commits.**

S: `git log --stat` will show the changed files.

P: **I want to create a new branch based on the current branch.**

S: `git checkout -b newbranchname` is for you.

P: **I hate a branch called "wth" and want to delete it.**

S: `git branch -d wth`.

P: **I want to change the name of a branch "wth" to "wtf".**

S: `git branch -m wth wtf` or checkout to the branch "wth" and use `git branch -m wtf`.

P: **Merge "goaway" branch to master branch.**

S: Checkout to master branch and `git merge goaway`.

P: **Merge conflicts?**

S: Check the conflicts using `git status`. Open up the conflict file and you will see.

P: **So hard to resolve the conflicts.**

S: `git mergetool` will use a graphical tool.
