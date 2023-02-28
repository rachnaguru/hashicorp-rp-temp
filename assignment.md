What is the difference between `git push`, `git pull`, and `git fetch`?

<ul>
<li>git push - sends changes from a local branch to a remote repository</li>
<li>git fetch - gets changes from a remote repository to your tracking branch</li>
<li>git pull -  gets changes from a remote branch to your tracking branch and merges them to a local branch</li>
</ul>

**Git Push**

`git push` takes your current branch and checks for a connection between your tracking branch and the remote repository. If so, it takes changes from your branch and pushes them to the remote repository. `git push` uses this methodology to ensure the remote branch resembles your local branch. However, this will only succeed if the remote branch has not diverged from your local branch. If it has, synchronize your local branch with the remote branch by using the `git pull` command or a combination of the `git fetch` and `git merge` commands.

**Git Fetch**

`git fetch` takes your current branch and checks for a tracking branch. If so, it looks for changes in the remote branch and pulls them to the tracking branch. Note that the `git fetch` command pulls the changes to the tracking branch, not the local branch. If you want to fetch them to the local branch, issue the command `git merge origin/master` (for the "master" branch). The `git merge` command integrates changes from another branch and merges them to your local branch.

**Git Pull**

`git pull` brings the content from a remote repository and immediately updates the local repository to match that content. It performs a `git fetch` followed immediately by `git merge`. 

**Note**

Use `git fetch` and `git merge` instead of `git pull` if you want to view the changes you are merging into your branch before the merge happens.
