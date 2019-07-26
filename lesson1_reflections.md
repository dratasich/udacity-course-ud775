How did viewing a diff between two versions of a file help you see the bug that was introduced?
---

- see changes, find mistakes
  (especially in large files)
- don't go over the whole code, concentrate on changes
  (typically the changes are much smaller than the whole file/code)

How could having easy access to the entire history of a file make you a more efficient programmer in the long term?
---

- in case of a bug, return to a working version
  (without freaking out, Denise won't get such a big crisis ;)
- see changes to learn from typical mistakes or wrong design decisions

What do you think are the pros and cons of manually choosing when to create a commit, like you do in Git, vs having versions automatically saved, like Google Docs does?
---

+ logical change -> one can easier follow the history
+ logical change -> one can easier relate bugs to changes
- forget to commit, changes have to be ordered later on which is sometimes annoying or even hard to do
- at the beginning, when not trained, commits are typically too big to be useful for bug-tracking

Why do you think some version control systems, like Git, allow saving multiple files in one commit, while others, like Google Docs, treat each file separately?
---

- code projects should be modular, i.e., split into several files for re-use
- a document is written in one file (with google docs or word) -- it actually depends on the editor and the size of the project

How can you use the commands git log and git diff to view the history of files?
---

`git log` lists the commit messages that are the logical changes over time
(from last changes to the beginning of the project)

`git diff` prints the change/difference between two commits, the details of the logical changes

How might using version control make you more confident to make changes that could break something?
---

- changes can be undone -> try out in a separate branch ;)

Now that you have your workspace set up, what do you want to try using Git for?
---

- this course ;)
- for each and every code project!
