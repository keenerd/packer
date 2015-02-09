apacman
==================

ArchLinux User Repository (AUR) helper and pacman wrapper forked from packer

Features:
* (**new**) Bug fix for saved AUR packages and --cachevcs
* (**new**) Bug fix for pacmatic
* (**new**) Build status log
* (**new**) Override EDITOR for PKGBUILDs in config file
* (**new**) --buildonly parameter to build but not AUR install packages
* (**new**) --nofail parameter to quit if a package does not build
* (**new**) --purgebuild parameter to remove unneeded build depends
* --skiptest to avoid installing unit test packages
* Config file support (/etc/apacman.conf)
* Cleaned up manpages
* Replacement for pacsysclean (-L list installed packages by size)
* -G now supports ABS + AUR packages
* --noaur parameter to skip AUR packages
* --warn parameter makes errors non-fatal (only enable if you know what you are doing)
* Run as root workaround for Pacman 4.2+
* All features from packer
* Saves built AUR packages to /var/cache/apacman/pkg
* Uses AUR package cache directory if applicable
* --needed parameter that does not install up-to-date packages
* --ignorearch parameter that ignores architectures specified in PKGBUILD (useful for ARM devices)
* --skipcache parameter that skips check for pre-built package in cache directory
* --cachevcs parameter installs cached VCS (git, svn, hg) packages newer than AUR PKGBUILDs
* Partial passthrough support for -R, -Q, and -U pacman parameters
