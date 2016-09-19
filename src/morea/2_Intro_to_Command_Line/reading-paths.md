---
title: "Paths"
published: true
morea_id: reading-paths
morea_summary: "An explanation of the UNIX file system and paths"
morea_type: reading
morea_sort_order: 6
morea_labels:
 - UNIX
 - file paths
---

# Paths

UNIX operating systems follow a hierarchical directory structure. Before I launch into an explanation of how the UNIX file system works, remember that in UNIX, **everything is a file**. Everything. Even outputs, commands, and devices are files. 

## File Systems

File systems are how your files are arranged in your computer.

![Image of UNIX file system](http://faculty.salina.k-state.edu/tim/unix_sg/_images/Unix_file_sys.png)

The UNIX file system looks like a tree, where everything starts in the root directory, which is just written as a forward slash: `/`. Basically, directories (also known as folders in other OSes) hold files and subdirectories, which hold even more files and subdirectories, and so forth. This tree of directories (and files) is easily navigable as long as you know the path of what you’re looking for.

## Paths

A *path* in the file system traces out the location of a file/directory from a given directory.

You separate directories with slashes which signifies if something is inside of something else. Remember, the very first slash is also a directory: the root directory. For example, `/home/john/Documents/DevLeague/helloworld.py` is the path detailing the location of the file “helloworld.py”. It is in the `DevLeague` directory, which is in `Documents`, which is in `john`, which is in `home`, which is in `/` (the root directory).

A special pathname is `~` (tilde). `~` stands for `/home/user/`. Note that `user` is not literally “user”, but the name of the user profile (which is `junior` in our computers at Academy). When you first open your terminal, you are placed in your user’s home directory `~` by default. It holds everything a normal user would use, the Desktop, Documents, Downloads, Pictures, etc. directories. In the above path example, we didn’t have to write out that entire path. Instead of having the `/home/user`, we could’ve just written `~/Documents/DevLeague/helloworld.py`. 

When writing out paths for anything (such as arguments), you can write them out as *absolute* or *relative* paths.

#### Absolute Paths

Absolute paths point to the file/directory regardless of the current working directory (the directory you are in). It always includes the root (or `~`). The paths in the examples above are written as absolute paths.

#### Relative Paths

Relative paths point to the file/directory starting from the current working directory. You write them without the root `/`, and just start off as if it’s continuing from where you currently are in your terminal. For example, if I am in `~/Documents` and I wanted to access the “helloworld.py” file, I could just write out `DevLeague/helloworld.py`.

---

[Click here](https://junior-devleague.github.io/JDLA-Web-Development/morea/2_Intro_to_Command_Line/experience-paths.html) to complete the experiential learning exercise “Tracing paths”.

Before moving on to the next reading, [click here](https://junior-devleague.github.io/JDLA-Web-Development/morea/2_Intro_to_Command_Line/experience-terminus.html) to complete the experiential learning exercise “Terminus”.

Then, [click here](https://junior-devleague.github.io/JDLA-Web-Development/morea/2_Intro_to_Command_Line/reading-basic-bash.html) to move on to the final reading of this module, “Basic Bash”.

<br>
