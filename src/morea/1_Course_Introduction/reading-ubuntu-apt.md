---
title: "Ubuntu & APT"
published: true
morea_id: reading-ubuntu-apt
morea_summary: "An introduction to the Linux distribution Ubuntu and how to install packages"
morea_type: reading
morea_sort_order: 3
morea_labels:
 - GNU/Linux
 - Ubuntu
---

# Ubuntu & APT

The computers here at Academy are loaded with the Ubuntu, the most popular distribution of Linux.

## Distributions

_Distributions_ (or just _distros_) are community/company-created OSes, using the Linux kernel and a package management system, that are freely distributed. So when people say they use Linux, they're actually using a distribution of it. All distributions of linux are essentially the same things, except with a few key differences:

- Default desktop environment (or DE, the desktop GUI you click around in, usually has a toolbar, icons, windows, folders, and taskbar)
- Default configurations (things like the settings and behaviors of the distro)
- Default packages (the software and programs it comes with)
- Release schedule (how often the packages are updated and released; either stable or rolling release)
- Package management system (explanation is literally two sentences later)
- The logo

### Package Managers

A package manager is a collection of software tools that automates installing, configuring, upgrading, and removing packages. They make it so you don't have to manually install everything yourself. They usually search through a repository (repo) for the given package, and then execute a set of steps to install it.

Repos are servers located around the world that contain sets of packages. Generally, the package manager gets its packages from the repo whose name it shares.

Each distro has its own package manager, and the distros that are forks of them (built on top of it and expanded from its source code to become its own distro). Some examples are:
 - Debian-based: apt
 - Arch-based: pacman
 - Red Hat-based: dnf
 - Gentoo-based: portage

## About Ubuntu

Ubuntu is a Debian-based distro that is known for being beginner-friendly and easy to use.  It uses _Unity_ as the default DE and `.deb` files as its packages. If you ever download a package from the internet that is `.deb`, you'd use the `dpkg` command to install it. For example, `dpkg -i chromium-widevine.deb`.

Ubuntu has a GUI for just about everything, and its creators boast that you never need to touch the comand line to use it. Despite this, we want you to **use the terminal as much as possible** to actually learn. If you stick with only using the GUI for everything, such as the Ubuntu Software application to install software, then you will become reliant on it and you won't be able to move on to other, more advanced distros like Arch Linux.

## APT

Apt (the Advanced Package Tool) is the package manager that comes with Debian-based distros, including Ubuntu. It accesses the apt repositories for its packages. `/etc/apt/sources.list` is the file that determines apt's sources (repos). When installing a package that requires other packages (which are known as _dependency packages_, because the installed package is dependent on them), it automatically resolves those dependencies and installs them with the package.

**When using apt on the computers here at Academy, make sure you only install approved software. If there is something you'd like to install, ask an instructor first!**

Some essential apt commands to manage your packages are:

Command | What it does
------- | ------------
`apt search [argument]` | searches the apt repo
`apt install [argument]` | installs the given package name
`apt remove [argument]` | removes the installed package
`apt purge [argument]` | completely removes an installed package and its configuration files
`apt autoclean` | removes `.deb` files for uninstalled packages
`apt clean` | removes all packages from the cache and reinstalls them
`apt autoremove` | removes dependency packages that are no longer needed
`apt update` | makes your source list up-to-date
`apt upgrade` | upgrades all installed packages to the latest version
`apt dist-upgrade` | the same as above, but it prioritizes more important packages in the case of a dependency conflict

<br>

**Whenever you would like to install software on any machine running Linux, do it from the package manager unless there is explicit instruction to do otherwise. This is the safest and best way to resolve dependencies and keep a clean computer.**

When installing a package, `apt search` it first to read the description and make sure it's the correct package name.

When uninstalling a package, skim the list of dependency packages to make sure nothing vital will be removed as well.

When you want to update your system and packages, it's recommended to execute the command `sudo apt update && sudo apt dist-upgrade`

---

[Click here](https://junior-devleague.github.io/JDLA-GNU-Linux-and-Python/morea/1_Course_Introduction/reading-what-is-python.html) to move on to the next reading, "What is Python?".

<br>
