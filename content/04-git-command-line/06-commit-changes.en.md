---
title: Committing Changes
weight: 6
---


### Commit changes locally to git

#### In Git, stage the new file you created

Moving back to Git, we can see whether Git has picked up that there is a new file in the repo.

We can check this by running `git status`:
```
$ git status
```
and the output should be something like:
```
On branch master
Your branch is up-to-date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	params/augustinus_vourinus.R

nothing added to commit but untracked files present (use "git add" to track)
```

There is one file containing changes and that it is the new parameters file you just created. At the moment, it is 'untracked' by git.

To **add (stage) this file to the commit** we are about to make, we'll use the `git add` command. Please **ONLY STAGE YOUR NEW FILE** (ie if for any reason you've accidentally edited any other file in the repo, please do not stage it).
```
$ git add params/augustinus_vourinus.R
```
It's a good idea to regularly use `git status` to get a picture of the state of the repository before doing anything. Let's do it now:
```
$ git status

On branch master
Your branch is up-to-date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   params/augustinus_vourinus.R
```
We can see that now we've staged the new file, it appears under "Changes to be commited".

<br>

#### Commit the staged file

The file has now moved to staging area. Were now ready to commit it. Before that we need to provide a **descriptive commit message** that explains what the changes contained in this commit are.

```
$ git commit -m 'a descriptive commit message'
```
Use the `git commit` command to commit the staged file(s), with the `-m` option to add a message. Running `git commit` without `-m` will open the default text editor for you to add a message, this is just a bit quicker for a short message.

By convention, commit messages are in the present tense. You can think of them as following the phrase "This commit will..". For instance:
```
$ git commit -m 'add params file for augustinus_vourinus'

[master bc57995] add params file for augustinus_vourinus
 1 file changed, 15 insertions(+)
 create mode 100755 params/augustinus_vourinus.R
```

The changes have now been committed locally to git but you still need to update your remote fork on GitHub. We'll do this by pushing our local changes to GitHub

<br>
