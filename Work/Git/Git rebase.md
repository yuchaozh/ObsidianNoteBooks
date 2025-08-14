[https://stackoverflow.com/questions/7929369/how-to-rebase-local-branch-with-remote-master](https://stackoverflow.com/questions/7929369/how-to-rebase-local-branch-with-remote-master)

After committing changes to your branch, checkout master and pull it to get its latest changes from the repo:

git checkout master  
git pull origin master

Then checkout your branch and rebase your changes on master:

git checkout RB  
git rebase master

...or last two commands in one line:

git rebase master RB

When trying to push back to origin/RB, you'll probably get an error; if you're the only one working on RB, you can force push:

git push --force origin RB

...or as follows if you have git configured appropriately:

git push -f

# Squash

[rebase - Squash my last X commits together using Git - Stack Overflow](https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git)

git rebase -i HEAD~5

# Stash

[git stash - How can I delete all of my Git stashes at once? - Stack Overflow](https://stackoverflow.com/questions/11369375/how-can-i-delete-all-of-my-git-stashes-at-once)

git stash clear

git stash list

git stash drop stash@{index}

Git stash untracked files

git stash --include-untracked

From <[https://stackoverflow.com/questions/835501/how-do-you-stash-an-untracked-file](https://stackoverflow.com/questions/835501/how-do-you-stash-an-untracked-file)>

# Revert a local commit made to the main branch:

git reset HEAD~   

From <[https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git?page=1&tab=scoredesc#tab-top](https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git?page=1&tab=scoredesc#tab-top)>

git reset <previous label or sha1>

[How can I undo pushed commits using git? - Stack Overflow](https://stackoverflow.com/questions/22682870/how-can-i-undo-pushed-commits-using-git)

# Clean both staged and unstaged files

git reset --hard && git clean -fd

From <[https://mattkomarnicki.com/articles/git-how-to-completely-discard-staged-and-unstaged-changes](https://mattkomarnicki.com/articles/git-how-to-completely-discard-staged-and-unstaged-changes)>