![](./DSCLogo.png)
# 1:CLI - [YouTube Link](-)

### Questions?
Hit me up at @ham on UQ's slack, https://slack.uqcs.org/
OR at h.bultitude@uq.net.au

## Introduction

Hello and welcome to the first lecture of UQ's partnership with Google - the  Developer Student Club initiative. My name is Hamish Bultitude, and today we will be going through the UNIX command line together. This lecture is intended for students that are in first and second year before taking CSSE2310, yet can act as a refresher if you are looking for it!

Note that this is indeed for the UNIX commandline (or CLI for short) - whilst there is *some* crossover with [windows systems](check), applicability of this lecture includes Linux, macOS and Windows Subsystem for Linux (WSL). Check online for info on how to install WSL if you are on windows, or you can login to UQs student computer - *MOSS* via SSH. 

Lets begin!

## General Terminal
Firstly, it is important to address why CLI is important. Previous to using the command line, you are probably used to running code from an IDE by the press of a button, or by moving around the filesystem by clicking through finder or windows explorer. Yet, by using the command line, it becomes easier to get tasks done faster & with greater clarity.

<Terminal History>

<Bash>

## Opening the terminal
The terminal should be pretty easy to find on all operating systems. 

`Terminal` - macOS & many Linux distros

`Command Line` or `cmd.exe` - Windows

Again, this is for UNIX systems, so the use of the command line program on windows will not be supported here. If you have installed WSL on windows, it should be fairly easily to open a new CLI. Check online for more information.

Either way, you should be dumped to a screen that looks similar to this...
<img src="./images/lecture1/bash.png" alt="drawing" width="500"/>

Congrats! *The hardest step to learning something is actually beginning*. 

## Moving around the filesystem
So without any prompts, what do we do now? Well, most likely (if you haven't fooled around with the CLI before) Bash has thrown you to your home directory. But what exactly is that? The home directory is 'your' space on the filesystem, for example, at UQ this is `/home/students/s1234567`, where you are free to edit files as you please. You can see whatever folder you are at currently using the `pwd` command - standing for *print working directory*.

We can create files at this folder by using the `touch <filename>` command. This will create a file within our home directory, as that is the current folder that we are in! 

We may want to create a new folder so we can better organise our files! This can be done with the `mkdir <name>` command. In case you were wondering, `mkdir` stands for *make directory*. 

What use is a folder if we cannot access it though? Enter the `cd <folder>` command, standing for *change directory*. Make sure to supply the full path of the directory that you want to access, or just the folder name if that folder is within the directory you are in! Confused? Have a play around with it :^)

We may want to 'free' ourselves from our home directory and step to the root of the filesystem. This can be done with `cd /` to move to `/` folder, aka the root of the filesystem. 

Whoops! We want to get back to the home directory! Just use `cd` to quickly move back to your home directory.

Before moving on, have a quick practice of moving around your filesystem. 

## Manual
If you ever get confused on how a command works, `man <command>` is your friend! For example, say we forget what the function of `ls` was? We could find out quickly with `man ls`. Most UNIX commands have an associated manual entry, yet let it be noted that some may not. At that point, dare I say, Google is your friend. 

There are a variety of numbers associated with `man`. These come into play when there are multple version of the same command - say `printf` is both a User Command and a C function.

1. User Commands
2. System Calls
3. C Library Functions
4. Devices and Special Files
5. File Formats and Conventions
6. Games et. Al.
7. Miscellanea
8. System Administration tools and Deamons

To separate out these, use `man <num> command` to be specific on the category of the command.

Whilst Google is pretty awesome, make sure you can understand the layouts and workings of the `man` command, probability says you are going to need it at least some point down the line.  

## What's in this folder: 1
After creating files and folders for a while, it becomes hard to remember exactly what is in a folder! Use `ls` to return whatever is in your current folder, or `ls <folder>` to see what is in the supplied folder.

## Flags: What's in this folder: 2
Flags are an important part of UNIX commands. The use of flags allows for extended functionality of certain commands. Some examples are seen below:

`ls -a`; lists ALL the files in the directory (including *hidden* files with the `.` extension (a la `.git/`). These files wouldn't be included with the normal `ls` command.
> ```
./              .DS_Store       1-CLI.md        3-AppEngine.md  README.md
../             .git/           2-GO.md         DSCLogo.png     images/
``` 
---

`ls -l`; lists regular files in a *detailed* view format. 
> ```
total 120
-rw-r--r--@ 1 hamishbultitude  staff   5549 18 Jul 20:07 1-CLI.md
-rw-r--r--@ 1 hamishbultitude  staff     24 15 Jul 17:59 2-GO.md
-rw-r--r--@ 1 hamishbultitude  staff     24 15 Jul 17:59 3-AppEngine.md
-rw-r--r--@ 1 hamishbultitude  staff  37470 15 Jul 18:04 DSCLogo.png
-rw-r--r--@ 1 hamishbultitude  staff    229 15 Jul 19:14 README.md
drwxr-xr-x  4 hamishbultitude  staff    128 15 Jul 19:29 images/
```
---

We can of course combine flags to specify further functions. See below:

`ls -a -l` or just simply `ls -al`
> ```
total 136
drwxr-xr-x  10 hamishbultitude  staff    320 18 Jul 20:14 ./
drwxr-xr-x@ 46 hamishbultitude  staff   1472 17 Jul 22:22 ../
-rw-r--r--@  1 hamishbultitude  staff   6148 15 Jul 19:29 .DS_Store
drwxr-xr-x  12 hamishbultitude  staff    384 18 Jul 20:08 .git/
-rw-r--r--@  1 hamishbultitude  staff   6685 18 Jul 20:14 1-CLI.md
-rw-r--r--@  1 hamishbultitude  staff     24 15 Jul 17:59 2-GO.md
-rw-r--r--@  1 hamishbultitude  staff     24 15 Jul 17:59 3-AppEngine.md
-rw-r--r--@  1 hamishbultitude  staff  37470 15 Jul 18:04 DSCLogo.png
-rw-r--r--@  1 hamishbultitude  staff    229 15 Jul 19:14 README.md
drwxr-xr-x   4 hamishbultitude  staff    128 15 Jul 19:29 images/
```
---

Make sure to check `man` for further info on flags for your favourite commands!

## Files
`cp` stands for copy, and believe it or not, allows you to copy files! Syntax is `cp <orig-file> <new-file>`.

-cp, mv, mv 2, rm

## The `alias` commmand 

## Whats going on?
-top, htop, kill

## `sudo`

## Vim vs Nano vs Emacs: The Eternal Battle

## IO (> and >>) 

## Pipes ( | ) 

## Grep

## Connecting to other computers (SSH)

## Running programs

ctrl C - Terminate Signal
ctrl D - EOF

## Version control (Git)

## Installing More Programs

## Esoteric Additions
-fish 

## Final thoughts
Thanks for listening through this lecture! Whilst using the CLI may be frightening, just 
