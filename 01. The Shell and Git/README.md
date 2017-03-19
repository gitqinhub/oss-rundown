# 01. The Shell and Git
This is a brief introduction to some core Linux shell commands as well as the Git VCS.
As always, look up the documentation and refer to it when necessary.
[Git Documentation](https://git-scm.com/documentation)

### Getting Started
If you haven't already, go ahead and clone/fork this repository (check the root README.md for details).

### Your first commits
Get started by ```touch```ing a file (it can be anything) and ```mv```ing it into this project folder.
Next, ```add``` the file to the Git stage, where you can then make sure everything is in order with ```status```.
Finally, ```commit``` the file with a message of your choosing, and, if you forked your own copy of the repository, ```push```
to update the master branch on Github's side.

### Fixing mistakes
Now, ```rm``` the new file you created, ```add``` it like previously, and then ```commit``` it to your Git repository.
Alas, you've just now decided this file is not actually trivial; how are you going to bring it back? Go ahead and ```revert```
the removal, committing this new change as well. Once you're all set, you can ```push``` if necessary.

### A new train of thought
Now hold on, you're thinking it's time to do some bugfixing. Of course, you could do that directly on the ```master``` branch,
but a smarter way to go about this would be to perform your little experiments in a separate environment. ```checkout``` a
```bugfix``` branch and switch to it. Edit your file's contents (making sure to create a nontrivial difference) and then commit
to this new ```bugfix``` branch. ```diff``` the ```bugfix``` branch and ```master``` branch and determine that your changes are
correct, and then ```merge``` the two branches. As usual, ```commit``` often, and ```push``` if you need to.

### Saving and emptying your work
```touch``` a new file, or edit the one already inside the repository. Should you decide to come back to these changes, you can
choose to ```stash``` these unstaged changes. From here, you can ```apply``` them again, or simply ```drop``` them. Should you
decide to trash the current work you've done in this branch, you have a couple options:
* ```git reset --hard [HEAD]``` will trash all current changes, including staged ones.
* ```git clean [-f]``` will irreversibly trash untracked files. It's quite useful for getting rid of temporary files,
but I recommend a ```--dry-run``` first if you decide to run this.
* ```git checkout .``` will trash your unstaged changes, leaving alone staged and untracked files.
* And, of course, you could simply ```stash``` and ```drop``` if you want to remove all the changes you've made since the last
commit.

### Further reading
There's quite a lot of Git commands, so don't be shy and take a look at all of them. The flags you can provide can also prove to be
quite useful, so don't hesitate to familiarize yourself with them. Finally, the documentation is always up-to-date, and StackOverflow
generally has answers to most common Git questions.