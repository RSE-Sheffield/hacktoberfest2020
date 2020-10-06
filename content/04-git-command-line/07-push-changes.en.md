---
title: Pushing Changes
weight: 7
---


### Push changes to your fork GitHub


Now that you have made the commit, let's check using `git status` (if you haven't already)

```
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

To push the commit to your fork on GitHub we'll use
```
$ git push origin HEAD
```
This tells git to push to your forked repo `origin` (which we can check by running `git remote -v`) using the current `HEAD` which will be at the commit you just made.

The output will be something like:
```bash
Counting objects: 4, done.
Delta compression using up to 12 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 599 bytes | 599.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:johndoe/collaborative_github_exercise.git
   e56c543..bc57995  HEAD -> master
```
