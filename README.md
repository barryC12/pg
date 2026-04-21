# pg

A simple, universal package manager wrapper for Linux.

pg provides a single consistent interface across Linux distributions while automatically using the correct system package manager.

Features:
- Unified commands across all major package managers
- Automatic detection on first run (saved to config)
- Optional helpers (nala for apt, paru for Arch)
- Fast and lightweight
- Reconfigurable anytime

Supported distributions:
- Debian / Ubuntu → apt / nala
- Arch Linux → pacman / paru
- Fedora → dnf
- openSUSE → zypper
- Gentoo → emerge
- Void Linux → xbps

Installation:

Manual install (recommended):

sudo apt install make git   # or equivalent for your distro

Clone and install:

cd ~
git clone https://github.com/barryC12/pg.git
cd pg
sudo make install

Quick install:

Make sure curl is installed:

curl -fsSL https://raw.githubusercontent.com/barryC12/pg/refs/heads/master/quick-install/inst.pg | sh

Usage:

pg -S firefox        install package
pg -Rm firefox       remove package
pg -Cl firefox       purge package
pg -I firefox        search packages
pg -Up               update package lists
pg -Ut               upgrade system
pg -Rec              reconfigure package manager
pg -H                show help

Configuration:
~/.config/pg/config.pg

Notes:
- paru must be installed manually on Arch Linux
- pg is a wrapper, not a replacement for system package managers
- Gentoo uses emerge and emerge -C
- Void Linux uses xbps
