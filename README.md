apacman
==================

ArchLinux User Repository (AUR) helper and pacman wrapper forked from packer

Features:
* (**new**) Replacement for pacsysclean (-L list installed packages by size)
* (**new**) Built-in ABS support (-G now support ABS+AUR packages)
* (**new**) --noaur parameter to skip AUR packages
* (**new**) --warn parameter makes errors non-fatal (only enable if you know what you are doing)
* (**new**) run as root workaround for Pacman 4.2+
* All features from packer
* Saves built AUR packages to /var/cache/apacman/pkg
* Uses AUR package cache directory if applicable
* --needed parameter that does not install up-to-date packages
* --ignorearch parameter that ignores architectures specified in PKGBUILD (useful for ARM devices)
* --skipcache parameter that skips check for pre-built package in cache directory
* --cachevcs parameter installs cached VCS (git, svn, hg) packages newer than AUR PKGBUILDs
* Partial passthrough support for -R, -Q, and -U pacman parameters
