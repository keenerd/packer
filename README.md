packer
======

A package manager utility for pacman repositories and the AUR. packer
is designed to be a faster, simpler replacement for yaourt. Unlike
yaourt, packer only handles tasks that may require access to the AUR,
or are required by tasks that do. For everything else, simply use
pacman.

Installation
------------

The easiest way to install packer is from the AUR. There is currently
no other installation script. If (for some odd reason) you want to
install it manually, simply copy the following files to the following
locations:

 * packer: /usr/bin/packer
 * packer.8: /usr/share/man/man8/packer.8
 * packer.bashcomp: /etc/bash_completion.d/packer
 * packer.zshcomp: /usr/share/zsh/site-functions/_packer

Usage:
------

packer's usage is similar to pacman, but there are a few differences.
One is that packer only supports the following actions and options:

### Actions

 * -S
   install
 * -Ss(q)
   search (quietly)
 * -Si
   get info about package
 * -Sc(c)
   delete cached files including ones from packer (delete more)
 * -S(y)u
   update (get new cache data)

### Options

 * --quiet
   same as the optional 'q' in -Ss(q)
 * --ignore
   a package to ignore
 * --noconfirm
   don't ask any questions
 * --asexplicit
   install packages explicitly
 * --asdeps
   install packages as dependancies
 * --noedit
   don't ask if the user wants to edit AUR files
 * --auronly
   only preform AUR-based actions
 * --devel
   add all VCS packages to the list of packages to be updated
 * --skipinteg
   skip makepkg's integrity checks
 * --aursort
   sort AUR search results alphabetically
 * --color
   colorize AUR actions, even when piping
 * -h, --help
   print a usage message
 * --
   assume all of the following arguments are packages

Another difference is the inclusion of an interactive mode. Running
packer with a package name (and options) but without specifying an
action will start interactive mode. In this mode a numbered list of
search results for the given package is displayed, and one or more
numbers are requested. Entering the coresponding numbers will
install those packages.

One last small difference is that, if sudo is installed, packer will
automatically prompt for you password when it needs. For security
reasons it is recommended you install and configure sudo properly,
and then run packer as a normal user, not as root. For more
information on sudo, take a look at [the ArchWiki's Sudo article]
[aw-sudo].

### Examples

To install a package:

	packer -S <package>

To search for a package:

	packer -Ss <keyword>

Install without confirmation:

	packer -S --noconfirm <package>

Search and install using interactive mode:

	packer <package>

Launch interactive mode, but install as dependencies:

	packer --asdeps <package>

Search for a package, colorize results, and display in less:

	packer -Ss --color <package> | less -R

Configuration
-------------

packer reads the following settings from /etc/pacman.conf:

 * IgnorePkg
 * DBPath

Both of these settings have the same effect on packer's operation as
they do on pacman. Obviously, if pacman is called it will read any
settings it needs.

If you want to edit a file, the $EDITOR environment variable is used.
If editor is not set, packer will use vi.

Output is colorized if pacman-color is installed.

diffpac
-------

If you've been using yaourt and just can't stop because of
pacdiffviewer then you should take a look at diffpac, a stand-alone
pacdiffviewer fork. If you don't like it, or want some of the other
features that that yaourt provides, you can always use both packer
and yaourt. Since packer is designed to only do what it needs to do,
it requires you to use at least pacman as well. There's no reason you
can't use it with something else (such as yaourt) too.

Authors
-------

 * Matthew Bruenig <matthewbruenig@gmail.com>

[aw-sudo]: http://wiki.archlinux.org/index.php/Sudo
