`git log`
---------

Now that you've made a change, lets look at the history of the repository. Run
`git log` to be shown all of the commits in the current branch. Each commit
looks something like this:

        commit f1db20ca0f0bdad39ccf473f3afc6e40dcf6df8e
        Author: Ayman El Didi <ayman@eldidi.org>
        Date:   Mon Feb 6 00:01:27 2023 -0700

            initial commit

It shows the author of the commit, the date it was made, and the message at the
bottom. The thing at the top labeled "commit" is a hash which uniquely
identifies the commit.

You can press the up and down arrows to scroll, and q to exit.

`push` and `pull`
-----------------

If you wanted to push your changes to Github, you'd run
`git push origin branchname`, which means "push my changes to the origin (which
is usually Github) on the branch named branchname".

If you don't specify origin and the branchname, it tries to push to the
"upstream", which is the default for your branch. To set upstream for your
branch, run `git push -u origin branchname`, and from then on you can just run
`git push`.

To bring in changes from another branch into yours, run
`git pull origin otherbranchname`. If the two branches cannot be automatically
merged together, you get what's called a merge conflict. That's what we needed
to fix in lab 4.

`git pull` is also how you get the newest version of the code. You should
always run `git pull origin main` before doing any work to ensure you have the
latest version of the code.

So what if I need to un stage a change?
---------------------------------------

To unstage a file, that is remove it after using `git add` to add it to your
next commit, run `git reset -- filename`. Note those two dashes, those are
important.

To unstage all files, run `git reset` by itself.

Merging changes from another branch
-----------------------------------

Now we're going to try and bring in changes from the branch `silly` into our
own branch.

Run `git merge silly` to try to merge the changes from silly into our branch.
Usually, this will just work, but sometimes there are issues.

In this case, you should get a merge conflict. This is just me going over and
hopefully explaining better how merge conflicts work (This is easiest in
VSCode).

Once you're done, push your changes to the Github page for this repo by running
`git push -u origin branchname`, putting your branch name instead of
`branchname`.

Now we'll move on to [part 3.](/part-3.md)
