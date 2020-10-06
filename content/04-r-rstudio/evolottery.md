---
title: Evolottery
weight: 3
---

# **Welcome to the evolutionary lottery of skull and beak morphology**

## **#EvoLottery**

*** 
<br>

#### **Beak and skull shapes in birds of prey (“raptors”) are strongly coupled and largely controlled by size.** 

- In this exercise, each participant will **fork a GitHub repo**, and **contribute a file** required to simulate the *evolutionary trajectory of an imaginary species' body size*.

- We'll use **GitHub to collate all species files** and **plot** them all up together at the end! We'll also **discover the skull and beak shapes** associated with each simulated species size.


####  Start!





## :computer: **Clone a GitHub repo**

###  Start with GitHub repo

<https://GitHub.com/RSE-Sheffield/collaborative_GitHub_exercise>

<img src="/images/r-rstudio/repo.png" width="700px" />

### **Fork  it** 

make your **own copy of the repository** on GitHub. Fork are linked and traceable

<img src="/images/r-rstudio/fork-1.png" width="700px" /> 


GitHub makes a **copy into your account**

<img src="/images/r-rstudio/fork-2.png" width="700px" />
 
<br>


### :vertical_traffic_light: **Clone repo** 

**copy repo link** to create a new Rstudio project from the repository.
    
<img src="/images/r-rstudio/fork-3.png" width="700px" />


### **Create new project in Rstudio**

<img src="/images/r-rstudio/newproj-1.png" width="700px" />


Checkout from **version control repository**

<img src="/images/r-rstudio/newproj-2.png" width="700px" />

Clone project from a **git** repository

<img src="/images/r-rstudio/newproj-3.png" width="700px" />

Paste **repo link copied from GitHub** into **Repository URL** field. Click **`Create Project`**. 

<img src="/images/r-rstudio/newproj-4.png" width="700px" />

Rstudio project now **contains all files from the GitHub repo.**

<img src="/images/r-rstudio/newproj-5.png" width="700px" />



# :vertical_traffic_light: **Make a change to the repo**

## make a copy of `params_tmpl.R`

open **`params/params_tmpl.R`**

<img src="/images/r-rstudio/edit-1.png" width="700px" />


<div class="inverse"><strong>SAVE AS NEW <code>.R</code> script in <code>params/</code> folder</strong></div> 

Use species name of your choice to name new file. 

<div class="alert alert-warning">Please ***DO NOT OVERWRITE*** **`params/params_tmpl.R`**.</div>

<img src="/images/r-rstudio/edit-2.png" width="700px" />

## :vertical_traffic_light: Edit file

Edit file with parameters of your choice and save.

<img src="/images/r-rstudio/edit-3.png" width="700px" />


### The parameters each participants need to supply are:

- **`sig2`:** A numeric value greater than 0 but smaller than 5

- **`species.name`:** a character string e.g. `"anas_krystallinus"`. Try to create a species name out of your name!

- **`color`:**  a character string e.g. `"red"`, `"#FFFFFF"` (Check out list of [**colours in R**](http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf))


**NB: remember to save the changes to your file**


# :vertical_traffic_light: Commit changes locally to git

In the *git* tab, select the **new file** you created and click **`Commit`**.

<div class="alert alert-warning">Please **ONLY COMMIT YOUR NEW FILE**</div>

<img src="/images/r-rstudio/commit-1.png" width="700px" />

Write an informative commit message and click **`Commit`**  

<img src="/images/r-rstudio/commit-2.png" width="700px" />

your new file has now been commited  

<img src="/images/r-rstudio/commit-3.png" width="700px" />

# Push changes to GitHub

on the *git* tab click ⇧  to **push changes to GitHub**

<img src="/images/r-rstudio/push-1.png" width="700px" />

changes have now been updated in the **GitHub repo**

<img src="/images/r-rstudio/push-2.png" width="700px" />

---

# :vertical_traffic_light: create pull request

In your repository, create **`new pull request`** 
to merge fork to master repo (ie the original repo you forked)

<img src="/images/r-rstudio/merge-1.png" width="700px" />

GitHub checks whether your requested merge creates any coflicts. 
If all is good, click on **`Create pull request`**

<img src="/images/r-rstudio/merge-2.png" width="700px" />

Write an informative message explaining your changes to the master repo administrators. Click on **`Create pull request`**

<img src="/images/r-rstudio/merge-3.png" width="700px" />

The repository owner will then review your PR and either merge it in or respond with some guidance if they spot a problem.

Check original repo to see **your merged changes**

<img src="/images/r-rstudio/merged.png" width="700px" />


We'll merge all contributions and [plot them together at the end!](https://rse.shef.ac.uk/collaborative_github_exercise/plot_trait_evolution.html) 


