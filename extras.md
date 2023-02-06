Lets say you wanted to change your last commit. There's 2 ways to do that.

1. Make the change you want to make, then run `git commit --amend`. This will
   allow you to change the commit message.

2. To uncommit something and put the changes back in the staging area, run
   `git reset --soft HEAD~n` where n is the number of commits you want to undo.

Note that after doing this, you have to `git push -f` instead of `git push`,
since you changed something which someone else may have been using. This means
that if you do this everyone else has to re-clone or run `git pull`, so its
reccomended you only do this on your own branch.
