Version Control
===============

+ undo button
+ easier to collaborate
+ when used to, more efficient
+ find mistakes faster (difference is shown with git; linux: diff -u, windows: FC file1.txt file2.txt)
+ manual saving is tedious!! and takes up space
+ tracking across files (not the changes in a single file, track a project) -> repository of files
+ for big projects -> develop in pieces
+ exploration, try out new things without breaking the code (e.g., in a new/separate branch)


Unix Command Line Basics!

[Atlassian get started](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)
[summary of git commands](https://www.atlassian.com/git/tutorials/svn-to-git-prepping-your-team-migration)


Checkpoints
-----------

logical change -> new checkpoint

Examples:
- fix a bug or typo
- change color
- add interface
- add message type in protocol

in git thats called a "commit"
commit = checkpoint
commit = snapshot of the files in a repository

each commit has
- commit ID = serial number
- commit message = description, see also
  [commit message conventions](http://udacity.github.io/git-styleguide/)

git checkout <commit id> = check out a previous version of a code

`HEAD` is a reference to the current commit applied to the working directory
(current point in history of the repository that is checked out)

commit as often as possible - the smaller the logical changes the easier to understand

Setup Workspace
---------------

- install [git bash](https://gitforwindows.org/)
- [name and email](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)
- `git config --global core.editor <editor-of-choice>`
- `git config --global merge.conflictstyle diff3` if you don't use a mergetool
  [diff3 explained](https://blog.nilbus.com/take-the-pain-out-of-git-conflict-resolution-use-diff3/)
- [nice bash prompt](https://gist.github.com/eliotsykes/47516b877f5a4f7cd52f)
- nice git log with
  `alias gitlog='git log --all --graph --decorate'`
- windows users: `git config --global core.autocrlf true`


Repository
----------

difference to a simple project directory: .git folder including meta-data


Branch
------

everytime you switch context

master branch (should always work)
develop to try out features
feature #1
bugfix #2


Merge
-----

merge branches to main branch (master)

`git pull origin master`
=
`git fetch origin`
`git merge master origin/master`


git status
----------

prints:
* ahead, if you are ahead of the history, i.e., created at least one commit more in comparison to origin
  (master > origin/master)
* behind, if the origin changed and you're back in history
  (master < origin/master)
* up-to-date, if the commits are the same in the local and remote repository
  (master = origin/master, both references point to the same commit)
* out-of-sync, if your local repo has a new commit and your remote repo another new commit too
  (master != origin/master, kind of a branch in history)


Conflicts
---------

"out of sync" ... local master and remote master have different new commits

typically happens when collaborating with others
(or when changing files directly on GitHub AND locally)

when the same line is modified -> merge conflict in <file>
- open <file>
- conflicts are marked as:
  ```
  <<<<<<< HEAD
  my changes
  |||||||
  original version where the changes are base on
  =======
  remote changes
  >>>>>>> origin/master
  ```
- merge the lines (or decide which version to use)
- close the <file>
- run `git add <file>` to stage the changes (make it ready for commit)
- run `git commit`


Pull Requests
-------------

let others check my changes before they are merged

- fork repository to collaborate
- make changes in a new branch (not master)
- push branch to GitHub
- in GitHub select new branch and click pull request
- select in which repo or branch this pull request should be merged to

- merging a pull request creates a new commit (GitHub doesn't do fast-forward merges)

typically the original repo will also evolve, possibly creating merge conflicts at pull requests
- therefore add a remote to your local repo: call it "upstream"
- when doing the pull request, be sure you are up to date with the upstream master

### Updating a Pull Request

if boss is not satisfied with the pull request / changes
he/she might force you to revise some things in your pull request

- fix the things locally and commit to the separate branch
- push the branch = update it on remote

### Conflicting Changes

- remote changes on master have to be pulled first (origin master or typically upstream master)
- feature branch merge with master (better rebase your feature branch on top of master)
- then push again
