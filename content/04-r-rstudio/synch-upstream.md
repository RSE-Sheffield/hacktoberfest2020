+++
title = "Synch with upstream repository"
weight = 5
+++


Now that everyone has contributed to the [**RSE-Sheffield** repository](https://github.com/RSE-Sheffield/collaborative_github_exercise) (the **upstream** repository), the `params/` folder contains a number of files, one for each successful pull request.

However your local copy of the repository only contains the template and your own file. 

> Q: How can I merge changes from the **upstream** repository to my **local** repository?

## Add upstream remote

### Check current remotes

We can check the urls of remotes currently linked to our local repo using `usethis::git_remotes()`.

``` r
usethis::git_remotes()
```
```
$origin
[1] "https://github.com/annakrystalli/collaborative_github_exercise.git"
```
We see that only my form is currently listed as a remote under the name `origin`. 

### Add the RSE-Sheffield repo as upstream

To add a new remote we need the https url of the upstream repo (the equivalent of the one we used to create our project from our fork through version control) which in this case is `https://github.com/RSE-Sheffield/collaborative_github_exercise.git`. 

We can then use `usethis::use_git_remote()` to set the upstream repository:

```r
usethis::use_git_remote(
    name = "upstream", 
    url = "https://github.com/RSE-Sheffield/collaborative_github_exercise.git")
```

We can check that everything was set correctly with `usethis::git_remotes()`

``` r
usethis::git_remotes()
```
```
$origin
[1] "https://github.com/annakrystalli/collaborative_github_exercise.git"

$upstream
[1] "https://github.com/RSE-Sheffield/collaborative_github_exercise.git"
```

### Synch with upstream

Finally, to synch with the upstream repository we can now use function `usethis::pr_pull_upstream()`. This fetches the master branch from the upstream repository and merges it into our own local master branch.

```r
usethis::pr_pull_upstream()
```
```
✓ Pulling changes from GitHub source repo 'upstream/master'
```

You should now have all participant files in the `params/` folder and will be able to generate all bird skulls if you run `plot_trait_evolution.Rmd` locally.

## Synch origin

To also synch your origin remote repository you can simply push the merged upstream changes up to GitHub.