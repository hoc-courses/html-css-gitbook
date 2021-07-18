---
description: >-
  As a software developer, it is important that you become familiar with using
  the CLI
---

# Terminal/CLI Intro

### Overview

In the old days, you didn't have a graphical user interface to interact with the computer's operating system. You had to issue commands through a terminal window.  This is called the **command line interface**, or **CLI**, because you enter one command at a time on a line in the terminal window.

Today, you have both options. The GUI makes many operations, such as viewing folders and files on your computer, very easy for novice users. However, it is often more efficient to perform command through the terminal.

As a software developer, it is important that you become familiar with using the **CLI**. Many software programs used by software developers can only be operated through the command line interface.  Additionally,  you can write software to run commands automatically, allowing you to automate repetitive tasks.  You will use it regularly in your daily work.

### Git Bash 

![](../.gitbook/assets/image%20%28173%29.png)

When you installed **git**, it also installed an application called **Bash \(Bourne Again Shell\)**, which provides a command line interface shell and some useful utilities for working with git repositories. We will use the Bash shell in this course.

Using the Bash shell, you can give commands to the computer, either one at a time from a terminal window, or by running a script containing multiple commands to automate tasks.

Some of the most frequent uses:

* navigate your computer to manage files and folders
* run programs that provide more functionality from the command line
* launch programs from specific directories
* consistent commands across computers \(Mac, Windows, Linux\)

### Launching Git Bash

To launch Git Bash, open your Windows Start menu and type **Git Bash**.

The shell will always display some standard information followed by a $ sign. The information before the $ sign includes your username and current directory. 

You enter commands by typing the command after the $ sign and hitting the enter key.

When the shell first comes up, it will default to your home directory, which has the alias **~**. To see where the home directory is, type the command **pwd** \(present working directory\).

![](../.gitbook/assets/image%20%28174%29.png)

### CLI - What is a Command?

A command is how you execute a program that performs a specific operation. Many of the CLI's built-in commands focus on working with files and directories, such as the operations that you are used to doing through the Graphical UI for exploring your file system.

When you install certain applications, they may also install programs that can be executed as commands from the CLI.  For example, git, the version control system that we installed, has a large number of commands for working with your git repository. We will learn about those in the next section.

**Command Syntax**

The basic syntax of a command: **command-name** \[arguments\] \[flags\]

**Some commands have no arguments.** You just type the name of the command. 

| command | purpose |
| :--- | :--- |
| **pwd** | present working directory |
| **ls** | list contents of directory |
| **clear** | clears the CLI window log |

**Some commands take one or more arguments.** You type in the name of the command followed by some more information to provide more information to the command.

| command | purpose |
| :--- | :--- |
| **cd** &lt;directory name&gt; | change directory |
| **mkdir** &lt;directory name&gt; | create a directory |
| **touch** &lt;file name&gt; | create a file |
| **mv** &lt;old file name&gt; &lt;new file name&gt; | rename file |

**Some commands require additional information, that is passed in with flags**,  such as rm -r &lt;directory&gt; \(the -r means remove recursively, or all the way down\). You can look up the commands to see how each operates in the cheat sheet included in the resource section below. 

| command  | purpose |
| :--- | :--- |
| rm -r &lt;directory name&gt; | removed the entire directory tree |
| ls -l | lists contents of directory with details |
| git commit -m"&lt;message&gt;" | passes a message to the command |

As you work with the commands, you will learn the rules for how each one works.  In the Resources section there is a link to a cheat sheet for the built-in commands. For application-specific commands, you would look for a cheat sheet summarizing the commands on their website.

### Useful Commands

| Command | Description |
| :--- | :--- |
| up/down arrows | allows you to cycle through previous commands to load and repeat commands. |
| clear | clears the terminal window |
| pwd | present working directory |
| ls | List files in the directory |
| ls -a | List files in the directory \(include hidden files\) |
| cd &lt;directory&gt; | change the directory |
| touch &lt;file&gt; | Create an empty file |
| echo "something" &gt; &lt;file&gt; | redirect the output of echo and create a file |
| echo "another thing" &gt;&gt; &lt;file&gt; | append a string to the file |
| mkdir &lt;directory&gt; | make a new directory |
| cd - | previous directory |
| cd .. | parent directory |
| cd / | change to the root directory |
| cat &lt;file&gt; | concatenate the file line by line and display it on the terminal |
| mv &lt;file&gt; | renames the file |

Your first homework assignment, which you will start during the first class, will be practicing some of these commands.

### Resources

{% embed url="https://learntocodewith.me/getting-started/topics/command-line/" %}

{% embed url="https://cheatography.com/davechild/cheat-sheets/linux-command-line/" %}

