apacman
==================

ArchLinux User Repository (AUR) helper and pacman wrapper forked from packer

Features:
* All features from packer
* Saves built AUR packages to /var/cache/apacman/pkg
* Uses AUR package cache directory if applicable [new]
* --needed parameter that does not install up-to-date packages
* --ignorearch parameter that ignores architectures specified in PKGBUILD (useful for ARM devices)
* --skipcache parameter that skips check for pre-built package in cache directory [new]
* --cachevcs parameter installs cached VCS (git, svn, hg) packages newer than AUR PKGBUILDs [new]
* Partial passthrough support for -R, -Q, and -U pacman parameters
