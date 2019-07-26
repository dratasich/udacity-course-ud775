When would you want to use a remote repository rather than keeping all your work local?
---

- keep it safe
- collaborate with others

Why might you want to always pull changes manually rather than having Git automatically stay up-to-date with your remote repository?
---

- to avoid unnecessary merges when others work on the code simultaneously

Describe the differences between forks, clones, and branches. When would you use one instead of another?
---

fork = clone on GitHub
* use to start a project on GitHub based on an existing repository (e.g., a code project)
+ cloned repositories stay connected / are linked
+ creator of the original repository can see work of people who cloned his/her repo
+ creator can include good changes from forkers

clone = create or copy a repository locally
* download an online repository
* use to start a project locally
* to collaborate, to push code into another users repository

branch = branch commit history
* develop a feature in a repository (used to explore new implementation ideas)
* if you're fine with the feature, put it back on the main branch (master)
+ to avoid local copies of the repository

What is the benefit of having a copy of the last known state of the remote stored locally?
---

* check if and how much my local version diverges (be able to do a git diff with the remote repository)

How would you collaborate without using Git or GitHub? What would be easier, and what would be harder?
---

Dropbox
* but when it comes to conflicts, you have to do things manually
* btw: never-ever create a git repo in your dropbox workspace

When would you want to make changes in a separate branch rather than directly in master? What benefits does each approach have?
---

* implement a feature
* try out something
* collaborate to another project via pull-requests

-> don't mess up the master branch
