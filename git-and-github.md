# Git & GitHub

The Git Commit Graph

* Has a directed acyclic graph \(DAG\) structure

The Repo as a Graph of Commits

* Commits store the changes
  * Identified by SHA-1 hash
* Each commit represents a snapshot of the codebase
* A path of commits represents its history

Branch Workflow

* Branching is used to create different lines of development
  * Features
  * Bug fixes
  * Experimental code
  * Releases
* Keep the master branch clean

Note: A branch is just a reference \(i.e., a pointer\) to a commit in the graph \(it is NOT another commit\)

Checking Out

* To specify which branch we should work on, we must checkout the branch
* The checked out branch is pointed to by the HEAD ref

Diverging Branches

* Inevitably, diverging branches will need to merge back together
* Three cases for branch merging:
  1. Fast Forward
     * One branch has changes
  2. Recursive
     * Non-conflicting merge
  3. Fix conflicts manually
     * Conflicting merge

Fast Forward

* Changes only happened in one branch \(since the branching point\)
* Git performs the merge by simply moving the earlier reference pointer

```text
$ git checkout master
$ git merge feature
Updating 85flh3g..bk30t54
Fast-forward
```

Recursive Merge

* Branches have diverged from a common ancestor
* The changes in the two branches are NOT conflicting
* Merge performed by creating a new commit with two parents, changes from both branches

```text
$ git checkout master
$ git merge feature
Auto-merging
```

Conflicting Merge

* Changes in the two branches are conflicting
* Auto-Merge not possible

```text
$ git checkout master
$ git merge feature
CONFLICT
Auto merge failed;
```

* Need to fix conflict by hand
* Once conflict is resolved in the file, commit the changes

```text
$ git add -A
$ git commit 'merged feature'
```

Other Important Git Commands:

* git stash
  * Used when you want to switch branches but not commit work on your current branch
  * Bring back stashed changes with **git stash apply/pop**
  * Use stashing if you're going to do anything that leaves unsaved changes vulnerable
    * i.e., git reset --hard &lt;COMMIT&gt;
    * reverse your commit by pointing branch to earlier commit
* git log
  * provides various view of repo history
* git diff
  * show changes between commits, files, indexes, etc.

Remote Repo

* A version of your codebase hosted somewhere else accessible via URLs
* Can have multiple names remotes
  * Default is called origin
* Associate remote URL with name:
  * git remote add origin &lt;REMOTE\_URL&gt;

Basic Remote Commands

* git clone
  * create a copy of a repo
  * gives name origin to remote from which you cloned
* git pull \(and fetch\)
  * download new data from a remote
  * fetch gets the data
  * pull also attempts to merge your local commits with the remote \(fetch + merge\)
  * Usually use pull, but beware of conflicts so make sure working directory is clean through git status first

Commit vs. Push

* git commit creates a node in the commit graph of your local repo
* git push creates node\(s\) in the commit graphs of some remote repo

GitHub, Fork

* Forking creates a copy of the repo on GitHub
  * the fork is a separate GitHub repo, assocaited with your GitHub account
  * allows multiple teams to work on their own copy of the same code without needing other instances
* Forking vs. Cloning
  * Cloning is creating a copy of the code on your local machine

How do you contribute work to a repo you have no write permission for?

* Create a **pull request**, and let someone who has write permission merge
  * This is how open-source software works
  * This is how sometime you submit your coding assignments

Pull Request

* Built-in support in Git, but GitHub simplified the process and added convenient web UI on top of it
* Request project maintainer\(s\) to pull changes from your fork into their repo
* Discussion is part of the pull-request
* Automatically wan about conflicts
* Can merge pull-requests directly from GitHub

Pull Request Great For Code Review

1. Rather than simply merging your feature branch locally, push it to GitHub
2. Submit a pull request from the feature branch to master branch

Common Workflow

* You create a pull request \(PR\)
* Your teammate\(s\) review the PR, make comments, etc.
* You fix whatever needs to be fixed, based on the review\(s\)
* Once everybody is happy, someone on the team merges the PR

