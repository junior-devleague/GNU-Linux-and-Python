---
title: "Superuser Do"
published: true
morea_id: reading-sudo
morea_summary: "An explanation of how to gain root access and use the sudo command"
morea_type: reading
morea_sort_order: 8
morea_labels:
 - Bash
---

# Superuser Do

When you try to execute a command in the terminal, you might get an error reading _Permission denied_. This happens because, as the error implies, you don't have the correct permissions to execute that command and access certain files or directories.

## Root vs user directories

Trying to access or change something in a directory that isn't yours (the user's) as the user isn't possible in Bash. The user files, aka anything you can access by just typing in the commands, are the files and directories inside of `/home/user/` (again, `user` is the name of the user, not actually `user`). Everything outside of `/home/user/` are root directories, which require _root_ or _admin_ permissions to access. You might have experience with this by running things as administrator in other OSes.

## Root access

Every installation of Linux comes with a root account (called `root`) that has admin/root permissions and access to everything inside of root directories. 

In order to gain root access, you must use the `sudo` command at the beginning of any command that attempts to access any non-user files. `sudo` stands for _superuser do_, which gives your user the superuser (or root account) permissions for the given command.

For example, attempting to install the browser Chromium with `apt install chromium-browser` will download a bunch of files into the `/usr/bin/`, `/usr/share/`, and `/usr/lib/` directories, all of which are non-user directories (since they aren't in `/home/junior/`). If you run the above command without root access, you will get a _Permission denied_ error, because regular users can't do anything that would cause the files within non-user directories to change. Thus, in order to install things, you need to begin the command with `sudo`, so the full command would be `sudo apt install chromium-browser`.

---

This reading concludes the second module, "Intro to Command Line". [Click here](https://junior-devleague.github.io/JDLA-GNU-Linux-and-Python/modules/basic-bash) to move on to the next module, "Basic Bash".

<br>
