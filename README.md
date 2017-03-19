# Open Source Software Rundown
This is a preliminary introduction to the world of open source software and development.
Projects are more or less self-contained within their folders, and they *are* intended to be done in the order given.
I'll most likely update this with some regularity, especially given the fast-paced nature of software in general, so bear with me.

# Setup
I *highly* recommend setting up a *nix environment such as the various flavors of Linux or OpenBSD; a Mac will suffice as well if you
can set up Brew. On Windows, Cygwin and the new Windows 10 Ubuntu environment both work, although to varying degrees of success;
ultimately if you're looking for the least painful experience, it's best that you start with Linux.

**Cygwin has several known issues regarding installations and packages so its best to avoid it, if you really want Windows then the new Win10 is the best choice**

### Linux Distros
There's a multitude of Linux distributions out there, all with varying pros and cons, but ultimately there's only a couple you should
realistically be looking at if you're getting serious about a good Linux distribution. Here are a couple off the top of my head, in no particular order:
* Arch Linux
	* This is the distribution I enjoy running the most personally as it's very barebones, but installation can be a pain and/or dangerous if you don't RTFM.
	* Uses the Pacman package system, which is somewhat different from other package managers but frankly very easy to use.
	* Bleeding-edge builds, which means you're going to be updating your system and managing system files quite often on your own time.
* Linux Mint
	* Uses the apt package manager (synaptic package manager) which is commonly claimed to be the easiest to use of them all.
	* Synaptic enables easier management of programs/packages and helps keep the system up to date through a similar interface to the programs panel in Microsoft Windows
	* Sometimes may not be the most up to date on the newest verisons of software which can be a bother
	* In addition theres a massive number of forums and sites dedicated to Mint and Ubuntu users online
* Ubuntu
	* See above.
	* Pretty easy to use and install as long as your reading comprehension is competent. `:^)`
	* Linux Mint and Ubuntu are almost identical besides the initial installation packages and their choice of desktop/windows managers.
* Fedora
	* Uses the RPM package system, which is quite different from the usual apt-get you'll see in most other distributions.
	* Similar to Arch Linux in that it's very bleeding-edge and requires much more knowledge of the system to maintain.
	* Actively maintained by Red Hat!
* Debian
	* One of the oldest distros, on which Linux Mint and Ubuntu are built on top of. Also uses the apt package manager.
	* Super super stable distribution, you won't run into a lot of crashes here.
* openSUSE
	* A fairly stable system similar to Debian and it's children; not too sure what else it features since I've never even met someone who uses openSUSE.
* Kali Linux
	* A penetration testing suite...?
* Steam OS
	* Actually just YetAnotherDebianDerivative. Also not exactly something you should run for development, but I suppose it is a Linux distribution.
* Gentoo
	* A very hardcore Linux enthusiast distribution, where everything is maintained by you, the user. I believe it comes in both Linux and BSD variants.

Of course, there's quite a lot of other, just as popular distributions, so take a look around to see what fits your needs. I'll always +1 Arch Linux =)

### Packages
The bare minimum you'll need to get started with this repository is Git, which is a distributed versioning control system by the original author of Linux.
In short, you just need to install Git through your particular package manager. This is most likely one of the following:
```
$ pacman -S git
$ apt-get install git
$ rpm -i(vh) git-xxx.rpm
$ pact install git
```
With ```sudo``` as necessary.

On Windows, you can install the Git command-line interface, which will give you Git Bash for Windows.

# Getting Started
If you're all set up, go ahead and clone this repository!
```
git clone https://github.com/chocolatemelt/oss-rundown.git
```

If you're feeling particularly special, you can fork it and clone your own particular ```oss-rundown``` repository. Just remember to set the upstream if you ever
decide to pull from this master branch:
```
git remote add upstream https://github.com/chocolatemelt/oss-rundown.git
```
In the future, you can then just run the following to pull from here:
```
git pull upstream master
```

Finally, I recommend having a folder specifically for Git projects (such as /home/whatever/git) but it's totally your call, and won't affect anything you do in this repository.
Further packages and installations are explained in the individual project READMEs.

# Contributors
[Kevin Zhang (chocolatemelt)](https://github.com/chocolatemelt)
[Ben Hu (BenjiHu)](https://github.com/BenjiHu)
