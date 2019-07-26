What happens when you initialize a repository? Why do you need to do it?
---

* creates the folder `.git` holding the meta-data for git
* there the history (in the form of diffs), branch names and heads, configs, etc. is saved

How is the staging area different from the working directory and the repository? What value do you think it offers?
---

* working directory: do the changes, current state of the files
* staging area: put here the changes that are worth to commit
* repository: finally save a logical change

in the staging area you can collect for a logical change
(note you might have made different logical changes, however, here you can commit them one-by-one)

How can you use the staging area to make sure you have one commit per logical change?
---

* `git add` the changes that correspond to one logical change

the best way to do this is with `git add -i`,
* interactively add changes via `patch` and select the files you want to check for changes
  (probably all if you're not sure)
+ you don't have to add the whole file

What are some situations when branches would be helpful in keeping your history organized? How would branches help?
---

* features, in particular, experimental features
* manage architectures (e.g., android version)
* manage releases

though it doesn't say in this lesson,
sometimes you also create a branch for a bugfix,
e.g., when you want to open a pull request for an original repository

How do the diagrams help you visualize the branch structure?
---

you see
* what parents each commit has
* what are the differences
* number of changes

What is the result of merging two branches together? Why do we represent it in the diagram the way we do?
---

* the merge commit includes the changes made in both branches

What are the pros and cons of Git’s automatic merging vs. always doing merges manually?
---

* manual merging is annoying
* but git auto-merge may include unnecessary code (e.g., twice the same function when merging branches of two coders implementing the same function but with different names)
