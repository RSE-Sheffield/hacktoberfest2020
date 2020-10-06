---
title: Cloning
weight: 4
---


### **Clone a repository using Git**

<br>

#### **Set up Git with your credentials**

Before using Git for the first time, you'll want to set it up with your details, so that GitHub knows who you are when you make your contributions.

Start by opening terminal (MacOS, Linux) or Git bash (Windows).

Type `git version` and hit 'Enter', to check git is installed correctly. If it is, we can get started.

Configure your git settings by using:
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
replacing `"John Doe"` and `"johndoe@example.com"` with your name and email address respectively - you should use the same email address as the one you made your GitHub account with.

#### **Clone your fork**

Now that you have a fork in your account, let's clone it (ie download a local copy) through Git.

Firstly, in your terminal, navigate to the directory where you'd like to place your code for this exercise. Initially, the terminal may open in your home directory. You can check where you are by typing the command `pwd` and pressing Enter; and the command `cd` (change directory) to move around. If you'd like to make a new directory you can use `mkdir`, for example:
```
$ pwd
/home/johndoe

$ mkdir hacktoberfest

$ cd hacktoberfest/
```

To clone the remote repo to your computer go to the green `Code` button on your fork's GitHub page and copy the HTTPS URL, run:
```
git clone <HTTPS URL>

# for example
$ git clone https://github.com/johndoe/collaborative_github_exercise
```
Git will then copy the repo into a folder with the same name as the repo, ie `collaborative_github_exercise` and it will print:
```
  Cloning into 'collaborative_github_exercise'...
  remote: Enumerating objects: 859, done.
  remote: Total 859 (delta 0), reused 0 (delta 0), pack-reused 859
  Receiving objects: 100% (859/859), 5.50 MiB | 989.00 KiB/s, done.
  Resolving deltas: 100% (395/395), done.
```

<br>

Now that you have a copy of the repo locally, you can have a look at it.
```
# Change into the directory:
$ cd collaborative_github_exercise/

# and have a look at what's in there:
$ ls

assets                               gif      LICENSE  plot_trait_evolution.html  README.md
collaborative_github_exercise.Rproj  gif.gif  params   plot_trait_evolution.Rmd
```
