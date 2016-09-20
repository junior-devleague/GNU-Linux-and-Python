---
title: "Basic Bash"
published: true
morea_id: reading-basic-bash
morea_summary: "An overview of basic Bash commands & syntax for file navigation & manipulation"
morea_type: reading
morea_sort_order: 7
morea_labels:
 - Bash
---

# Basic Bash

Before this reading, [follow this link](https://junior-devleague.github.io/JDLA-GNU-Linux-and-Python/morea/2_Intro_to_Command_Line/experience-terminus.html) and complete the experiential learning exercise “Terminus”.

In Terminus, you performed spells, interacted with items, and traveled to different locations. These are all translatable to Bash, with the spells as commands, items as files, and locations as directories.

## Basic Bash commands

- `cd [directory]` - change directory into _[directory]_.
- `ls [directory]` - list out the contents of the _[directory]_. _If no argument is given (you just type out `ls`), it defaults to the current working directory_.
  - Note that files whose names begin with a dot `.` are hidden and ignored by `ls`.
- `pwd` - print working directory. Prints out the path of the current working directory.
- `touch [file]` - create a file named _[file]_.
- `mkdir [directory]` - make a directory named _[directory]_.
- `cp [files] [destination]` - copies the file to the destination.
- `mv [files] [destination]` - moves the file to the destination. Note that if the destination is the same as the source, _then it renames the file_.
  - Ex. `mv john.jpg headland.jpg` doesn’t move _john.jpg_ anywhere, it renames it to _headland.jpg_
- `rm [files]` - permanently removes the files.
- `rmdir [directory]` - removes the directory, as long as it is empty.
- `less [file]` - read and display the contents of the file.
- `cat [files]` - concatenates (combines) and prints the files directly into the terminal. Useful for redirection.
  - Ex. `cat file1 file2 file3` combines the contents of _file1_, _file2_, & _file3_ into a single output and prints it into the terminal.
- `file [file]` - displays information about the _[file]_, including its file format.
  - In Linux, filenames don't require a file extension (i.e. _.txt_, _.png_, etc.) to define its file format (file type). That is determined in the bits & data within the file.

When a command takes in a file/directory name as an argument, you can write out a path instead of only file names in your current working directory. For example, if you are in `~`, you can `cd Desktop/JohnHeadland/BashExercises/` instead of doing `cd Desktop`, `cd JohnHeadland`, and then `cd BashExercises`.

**Remember that case sensitivity matters!** `CD` is not the same as `cd`. The same goes for file/directory names. "_documents_" is not the same as "_Documents_".

## Bash syntax

Syntax is the structure any language must follow. Even Bash has a general syntax its commands follow (although some commands have their own):

**`command`** _`-option`_ `[argument]`

The **`command`** is the command that Bash executes. For example, `cd`, `touch`, `mkdir`

The _`option`_ is written after a dash `-`. It allows you to undergo different ways of executing the command. For example, `ls -a` (the _a_ option lists all files, including hidden ones whose names begin with a dot, .). You can use multiple options at once by directly appending them, a la: `pacman -Syu` (this uses the _-S_, _-y_, and _-u_ options all at once).

The `argument` is whatever you’re passing into the command. For example, `cd Desktop` passes in the _Desktop_ argument to be cd’d into.

**Use spaces to separate commands, options, and arguments**. Do **NOT** use spaces otherwise, such as for file or directory names, as they will be read as separate arguments. For example, `touch My file` will not create a single file called “My file”, it will touch two separate files named “My” and “file”.

## The manual

If you don’t know how to use a command, read the manual for that command by typing in **`man command`**, where **command** is the name of the command you would like to read about. It tells you the syntax for that command with its possible options (and what they do) and what to pass in for arguments. If you try using a command and something doesn’t work, or you have a question, read the manual.

## Autocompletion

When typing in arguments, you can use autocompletion with the **Tab** key. After typing in a unique amount of characters, if you press Tab, it automatically fills out the rest of the name for you! For example, if you’re in `~` and type in `cd Doc` and then press Tab, the shell will automatically fill out the rest for you as `cd Documents`.

---

### _A quick crash course on file system navigation_

- `cd [directory]` will bring you to a certain directory
- `ls` will list the contents of your present directory, so you can decide which folder to `cd` into next. **If you don’t know where to go, use `ls`**.
- If you don’t know where you are, use `pwd` (or read the path next to your _user@host_ in your terminal)
- **`..`** is the previous directory, and **`.`** is the current directory
  - `cd ..` will take you one directory up on the file system to go backwards.
      - Ex. You’re in `~/Desktop/JDLAWebDev`; `cd ..` will change directory to `~/Desktop`
- You can `cd` past/back multiple folders at once if you know the path. Just use slashes to separate the directories.
  - For example, if you’re in `~/Desktop/LinuxPython/JohnHeadland` and you want to get to `~/Desktop/WebDev/IreneFang`. You could type out the entire path, or just `cd ../../WebDev/IreneFang`.
- Tab completion is your friend. It makes things much faster and easier for you so you don’t have to type out the entire name of files and directories.

---

[Click here](https://junior-devleague.github.io/JDLA-GNU-Linux-and-Python/morea/2_Intro_to_Command_Line/experience-file-creation.html) for the experiential learning exercise that puts what you’ve just learned into practice.

[Click here](https://junior-devleague.github.io/JDLA-GNU-Linux-and-Python/morea/2_Intro_to_Command_Line/experience-treasure-hunt.html) to do the final experiential learning exercise of the module, “Treasure Hunt”, before moving on to [Module 3, “”](https://junior-devleague.github.io/JDLA-GNU-Linux-and-Python/modules//).

<br>
