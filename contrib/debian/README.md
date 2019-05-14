
Debian
====================
This directory contains files used to package bettyd/betty-qt
for Debian-based Linux systems. If you compile bettyd/betty-qt yourself, there are some useful files here.

## betty: URI support ##


betty-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install betty-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your bettyqt binary to `/usr/bin`
and the `../../share/pixmaps/betty128.png` to `/usr/share/pixmaps`

betty-qt.protocol (KDE)

