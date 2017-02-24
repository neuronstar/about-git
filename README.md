# about-git and GitHub



## What is special in git

"stage" (git add ), "commit" (git commit ) and "push" (git push) are the three steps. "stage" is like a dry run and tells git what to commit.
Here are the commands:
```
git add .
git commit -m "your message."
git push
```

## FAQ

Q: **I am too lasy to type in `git add .`.**

A: The magic potion is `git commit -a` which will do the staging and commit at the same time, for the files you have already staged.

Q: **What has been changed since last stage?**

A: `git diff` shows that.

Q: **I typed in the wrong commit message.**

A: `git commit --amend` will allow you to change the commit message you typed in before.

Q: **I forgot to add some files.**

A: Just add the file and use `git commit --amend`. This will allow you to replace the previous commit.

Q: **I accidentally added a file to staging.**

A: Should unstage the file. `git reset HEAD filename.md` will do.

Q: **I want to discard the changes I made since last commit.**

A: **This can be dangerous.** `git checkout -- filename.md` can revert averything back to the last commit. But it discards all the changes and can not be recovered. DO NOT USE IT.

Q: **I need to check what has changed in every commits.**

A: `git log --stat` will show the changed files.

Q: **I want to create a new branch based on the current branch.**

A: `git checkout -b newbranchname` is for you.

Q: **I hate a branch called "wth" and want to delete it.**

A: `git branch -d wth`.

Q: **I want to change the name of a branch "wth" to "wtf".**

A: `git branch -m wth wtf` or checkout to the branch "wth" and use `git branch -m wtf`.

Q: **Merge "goaway" branch to master branch.**

A: Checkout to master branch and `git merge goaway`.

Q: **Merge conflicts?**

A: Check the conflicts using `git status`. Open up the conflict file and you will see.

Q: **So hard to resolve the conflicts.**

A: `git mergetool` will use a graphical tool.

Q: **How do I revert almost anything?**

A: Read the article: [How to undo (almost) anything with Git](https://github.com/blog/2019-how-to-undo-almost-anything-with-git).


## GitHub

Q: Do I have to type in username and password everytime I clone or push?

A: No. Use [cache for https](https://help.github.com/articles/caching-your-github-password-in-git/) or [ssh key for ssh](https://help.github.com/articles/set-up-git/#next-steps-authenticating-with-github-from-git)
