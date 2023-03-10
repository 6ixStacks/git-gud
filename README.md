Configuring `git`
-----------------

First thing we'll do is set up git so we can use it normally. We'll have to set
our email address and real name which will be listed on our commits. Run these
commits:

```
git config --global user.name 'Ayman El Didi'
git config --global user.email ayman@eldidi.org
```

We can alo set which editor we use for when we run `git commit`. If you want to
use VSCode, run the command below. If not, replace 'code --wait' with the name
of the editor you use.

```
git config --global core.editor 'code --wait'
```

Getting Started
---------------

Everything we'll be doing here will be on your own branch. To create a new
branch, run `git switch -c branchname`.

To switch to a branch that already exists, use `git switch branchname`.
After creating your branch, you should see some output like:

        Switched to a new branch 'silly'

Now open up `names.txt` and add your name to the bottom.

You should see something like this:

        On branch silly
        Changes not staged for commit:
          (use "git add <file>..." to update what will be committed)
          (use "git restore <file>..." to discard changes in working directory)
        	modified:   names.txt

        no changes added to commit (use "git add" and/or "git commit -a")

It says we've changed `names.txt`. You now need to add the change to your
staging area and commit it.

Staging and Committing
----------------------

The staging area is the set of changes which will be part of the next commit.
It exists for when you make a handful of unrelated changes but don't
necessarily want to commit them all at once.

To add something to the staging area, use `git add filename`. After doing that,
run `git commit` to open VSCode on the commit you want. Running `git add .`
adds all files in the current folder to the staging area.

There you can type in your commit message. When the file is saved and closed,
git will make the commit with the message you typed.

As a shorthand, `git commit -m 'some message'` can be used to write a commit
without opening the editor, and `git commit -a` adds all files to the staging
area before committing automatically.

Now we'll move on to [part 2.](/part-2.md)
