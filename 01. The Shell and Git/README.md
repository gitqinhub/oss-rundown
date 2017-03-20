# 01. The Shell and Git
This is a brief introduction to some core Linux shell commands as well as the Git VCS.
As always, look up the documentation and refer to it when necessary.
[Git Documentation](https://git-scm.com/documentation)

### Getting Started
If you haven't already, go ahead and clone/fork this repository (check the root README.md for details).

### Your first commits
Get started by ```touch```ing a file (it can be anything) and ```mv```ing it into this project folder.
Next, ```git add``` the file to the Git stage, where you can then make sure everything is in order with ```git status```.
Finally, ```git commit``` the file with a message (```-m```) of your choosing, and, if you forked your own copy of the repository, ```git push```
to update the master branch on Github's side.

### Fixing mistakes
Now, ```rm``` the new file you created, ```git add``` it like previously, and then ```git commit``` it to your Git repository.
Alas, you've just now decided this file is not actually trivial; how are you going to bring it back? Go ahead and ```git revert```
the removal, committing this new change as well. Once you're all set, you can ```git push``` if necessary.

### A new train of thought
Now hold on, you're thinking it's time to do some bugfixing. Of course, you could do that directly on the ```master``` branch,
but a smarter way to go about this would be to perform your little experiments in a separate environment. ```git checkout``` a
```bugfix``` branch and switch to it. Edit your file's contents (making sure to create a nontrivial difference) and then commit
to this new ```bugfix``` branch. ```git diff``` the ```bugfix``` branch and ```master``` branch and determine that your changes are
correct, and then ```git merge``` the two branches. As usual, ```git commit``` often, and ```git push``` if you need to.

### Saving and emptying your work
```touch``` a new file, or edit the one already inside the repository. Should you decide to come back to these changes, you can
choose to ```git stash``` these unstaged changes. From here, you can ```git stash apply``` them again, or simply ```git stash drop``` them. Should you
decide to trash the current work you've done in this branch, you have a couple options:
* ```git reset --hard [HEAD]``` will trash all current changes, including staged ones.
* ```git clean [-f]``` will irreversibly trash untracked files. It's quite useful for getting rid of temporary files,
but I recommend a ```--dry-run``` first if you decide to run this.
* ```git checkout .``` will trash your unstaged changes, leaving alone staged and untracked files.
* And, of course, you could simply ```stash``` and ```drop``` if you want to remove all the changes you've made since the last
commit.

### Further reading
There's quite a lot of Git commands, so don't be shy and take a look at all of them. The flags you can provide can also prove to be
quite useful, so don't hesitate to familiarize yourself with them (```man git```). Finally, the documentation is always up-to-date, and StackOverflow
generally has answers to most common Git questions.
