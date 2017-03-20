# 02. Configuring the System
This is a brief introduction to the .conf / rc dotfiles you'll typically come across when using *nix programs.

### Getting Started
If you can access any of the *nix style shells such as ```Bash```, ```Zsh```, ```fish```, or any of the other shells provided online, you should be all set.
Other programs that use .conf/rc style dotfiles include ```tmux```, ```emacs```, ```vim```, ```taskwarrior```, ```xorg```, ```pulseaudio```, ```alsa```, among many others.

### What are they?
.conf / rc dotfiles are files used to configure various *nix programs on your computer. Their syntax is generally very similar;
that being said, do check with the documentation to make sure you're complying with their standards. Generally, they lie within your
home directory, and have names such as:
```
.tmux.conf
.vimrc
.zshrc
.bashrc
.taskrc
.xinitrc
.config
```
One important thing to note here is that they all generally start with a dot, which is why most people generally refer to them as *dotfiles*.

### Finding your dotfiles
A special feature of most major operating systems is that they hide files that begin with a dot by default; these are files that are
generally hidden because they're *system files*. Naturally, the configurations for your various programs are hidden as well. To see them
with `ls`, add `-a` to show all files

Note the `.` and `..` folders, which are your current and parent directory.

### Editing your dotfiles
I can't possibly provide examples for every unix program under the sun, but you can look at them on a case-by-case basis; simply *read
the documentation*. Especially larger programs such as the X server and Vim have very descriptive documentation for their dotfiles,
if you're looking in the right places. Generally, you'll have to reload a program after editing its dotfile to see any changes. This can
come in the form of restarting it or simply running a command that refreshes it's settings (such as most shells).

### Syncing your dotfiles
Knowing that your dotfiles are always going to be in the same place (namely, `~`), syncing your dotfiles across platforms is not only easy
but also highly recommended.
1. Start by creating a new repository; you can sync it to whichever hosting service you like (most likely GitHub, but BitBucket is my favorite
alternative personally).
2. `mv` your files to the repository you just created; careful not to reload anything just yet.
3. `ln -s` each file from your repository back to your home; this creates a symlink to the repository, and you will be able to commit
and push changes to your dotfiles as with any other repository and still update it at the same time. The `ln -s` command takes the source
file first, then the target file. You can easily script this in Bash for future machines, so you don't have to repeat the commands:
```
/bin/sh
ln -s /your/repo/here/zshrc ~/.zshrc
ln -s /your/repo/here/vimrc ~/.vimrc
...
```
