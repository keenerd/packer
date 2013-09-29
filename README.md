apacman
==================

ArchLinux User Repository (AUR) helper and pacman wrapper forked from packer

Features:
* All features from packer
* Saves built AUR packages to /var/cache/apacman/pkg
* --needed parameter that does not install up-to-date packages
* --ignorearch parameter that ignores architectures specified in PKGBUILD (useful for ARM devices)
* Partial passthrough support for -R, -Q, and -U pacman parameters
