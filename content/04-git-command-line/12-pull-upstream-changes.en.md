---
title: Pulling Upstream Changes
weight: 12
---

Now that everyone has contributed to the [**RSE-Sheffield** repository](https://github.com/RSE-Sheffield/collaborative_github_exercise) (the **upstream** repository), the `params/` folder contains a number of files, one for each successful pull request.

However your local copy of the repository only contains the template and your own file.

> Q: How can I merge changes from the **upstream** repository to my **local** repository?


### Add the **Upstream** Remote repository

First, we have to configure `git` to know where our **upstream** repository is located by running
```
$ git remote add upstream https://github.com/RSE-Sheffield/collaborative_github_exercise.git
```
to add a remote repository named `upstream` at the URL `https://github.com/RSE-Sheffield/collaborative_github_exercise.git`.
We can check that this worked using the following
```
$ git remote -v

origin	git@github.com:johndoe/collaborative_github_exercise.git (fetch)
origin	git@github.com:johndoe/collaborative_github_exercise.git (push)
upstream	git@github.com:RSE-Sheffield/collaborative_github_exercise.git (fetch)
upstream	git@github.com:RSE-Sheffield/collaborative_github_exercise.git (push)
```
This tells us the names of the remote repositories we have configured `origin` and `upstream` and their URLs.


### Pull upstream changes

To pull the upstream changes from the **`RSE-Sheffield`** repository, run the following commands
```
# check out the master branch
$ git checkout master

# fetch commits from all configured remotes and remove any unused tracking branches
$ git fetch --prune --all

# merge commits from the `upstream/master` branch into your local `master` branch
$ git merge upstream/master
```
Git's default behaviour is to add these commits to the master branch in what is known as a "fast-forward merge". Find out more about [fast-forward git merging](https://ariya.io/2013/09/fast-forward-git-merge).



### Push changes to your **origin** remote

The **origin** remote is **your fork of the repository** that's labelled with your GitHub profile avatar.

If we run:
```
$ git fetch --prune --all
# followed by
$ git status
```
We can see that your local repository **is now lagging behind** the upstream remote. That's because it's still missing all the files contributed by the other participants.

To update your **origin** remote with commits from the upstream repo, **Push**  the changes you've just fetched into your local repository by running:
```
$ git push origin HEAD
```

> ### Once you've pushed, all the repositories should now be showing as synced. :tada:

## Run the analysis (optional)

To run the analysis, open the project in Rstudio, click on the `plot_trait_evolution.Rmd`, then click on the Knit button. This should render including everybody's species! See more on [Rmarkdown notebooks](https://rmarkdown.rstudio.com/authoring_quick_tour.html#Overview)
