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

Use your GitHub username and and the email you used to sign-up on GitHub

```{r eval=FALSE}
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

To avoid having to type in your GitHub username and password every time you want to push an edit when using Rstudio interactively, you can set up an **SSH RSA key** 

### Create SSH key

On the top toolbar of your Rstudio, click “Tools” and select “Global Options…” from the dropdown menu

![](/images/r-rstudio/ssh-create.png)

### Add public key to GitHub

#### Copy public key from Rstudio

Once you've created your SSH RSA key pair, you need to add the public key to GitHub. To do so, in Rstudio, click on **View public key** (see image above) and **copy the text in the pop up tab**.

![](/images/r-rstudio/ssh-copy_public.png)

#### Got to profile settings on GitHub

**Navigate to GitHub**, click on your profile avatar on the top right corner and, on the drop down menu, select **Settings**

![](/images/r-rstudio/ssh-github_profile.png)

#### Open the SSH and GPG key tab

Navigate to the **SSH and GPG key tab** on the left hand side menu and click on **New SSH key**

![](/images/r-rstudio/ssh-add_ssh.png)

#### Create new SSH key and save

In the new SSH key tab that opens, give the key a title that indicates the machine your private key is stored on and **paste the SSH key in the key field**

![](/images/r-rstudio/ssh-save.png)