# DanctNIX Package Source

This repo holds all PKGBUILD from the DanctNIX [repos](https://archmobile.mirror.danctnix.org).

## Build instructions

```
$ sudo -e /etc/pacman.conf # setup localrepo "[archlinux-sxmo]\nSigLevel = Optional TrustAll\nServer = file:///home/archlinux-sxmo-repo"
$ sudo mkdir -p /home/archlinux-sxmo-repo
$ sudo chown $USER:$USER -R /home/archlinux-sxmo-repo/
$ rm -rf /home/archlinux-sxmo-repo/*
$ repo-add /home/archlinux-sxmo-repo/archlinux-sxmo.db.tar.gz
$ sudo pacman -Sy
$ PARU_CONF=/dev/null paru -B --localrepo=archlinux-sxmo --chroot=~/archlinux-sxmo-chroot packages/*
```
