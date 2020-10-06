+++
title = "Set up Git for R and Rstudio"
date =  2020-10-06T10:54:55+01:00
weight = 2
+++


# :computer: Configure git & GitHub

## Install package `usethis`


```r
install.package("usethis")
```

## Configure git

First, `git` needs to know who you are so your commits can be attributed to you. **`usethis`** to the rescue again!

**Check your configuration**

```r
usethis::use_git_config()
```


**Set your configuration**

Use your github username and and the email you used to sign-up on GitHub

```r
usethis::use_git_config(
    user.name = "Jane",
    user.email = "jane@example.org")
```




## :vertical_traffic_light: Set up GITHUB PAT


To authenticate with GitHub through the GitHub API (for example when you want to create a repo programmatically), you'll also need a Personal Authorisation Token (PAT).

```r
usethis::browse_github_pat()
```

will open up the GitHub panel to generate your PAT. 


<img src="/images/r-rstudio/browse_github.png" height="300px">


---

Copy it and paste it into your `.Renviron` file as system variable `GITHUB_PAT`.

```r
usethis::edit_r_environ()
```

Use `edit_r_environ()` to open and edit your `.Renviron` file

![](/images/r-rstudio/GITHUB_PAT.png)
----

## OPTIONAL: Set up SSH key

To avoid having to type in your GitHub username and password every time you want to push an edit when using Rstudio interactivelly, you can set up an **SSH RSA key** 

### Create SSH key

On the top toolbar of your RStudio, click “Tools” and select “Global Options…” from the dropdown menu

![](/images/r-rstudio/ssh-create.png)

###
