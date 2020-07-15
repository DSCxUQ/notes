![](./DSCLogo.png)
# 1:CLI - [YouTube Link](-)

### Questions?
Hit me up at @ham on UQ's slack, https://slack.uqcs.org/
OR at h.bultitude@uq.net.au

## Introduction

Hello and welcome to the first lecture of UQ's partnership with Google - the  Developer Student Club initiative. My name is Hamish Bultitude, and today we will be going through the UNIX command line together. This lecture is intended for students that are in first and second year before taking CSSE2310, yet can act as a refresher if you are looking for it!

Note that this is indeed for the UNIX commandline - whilst there is *some* crossover with [windows systems](check), applicability of this lecture includes Linux, macOS and Windows Subsystem for Linux (WSL). Check online for info on how to install WSL if you are on windows, or you can login to UQs student computer - *MOSS* via SSH. 

Lets begin!

## General Terminal
Firstly, it is important to address why CLI is important. Previous to using the command line, you are probably used to running code from an IDE by the press of a button, or by moving around the filesystem by clicking through finder or windows explorer. Yet, by using the command line, it becomes easier to get tasks done faster & with greater clarity.

<Terminal History>

<Bash>

## Opening the terminal
The terminal should be pretty easy to find on all operating systems. 
`Terminal` - macOS & many Linux distros
`Command Line` - Windows
Again, this is for UNIX systems, so the use of the command line program on windows will not be supported here. If you have installed WSL on windows, it should be fairly easily to open a new CLI. Check online for more information.

Either way, you should be dumped to a screen that looks similar to this...
<img src="./images/lecture1/bash.png" alt="drawing" width="500"/>

Congrats! *The hardest step to learning something is actually beginning*. 

## Moving around the filesystem
So without any prompts, what do we do now? Well, most likely (if you haven't fooled around with the CLI before) Bash has thrown you to your home directory. But what exactly is that? The home directory is 'your' space on the filesystem, for example, at UQ this is `/home/students/s1234567`, where you are free to edit files as you please. You can see whatever folder you are at currently using the `pwd` command - standing for *print working directory*.

We can create files at this folder by using the `touch <filename>` command. This will create a file within our home directory, as that is the current folder that we are in! 

We may want to create a new folder so we can better organise our files! This can be done with the `mkdir <name>` command. 

What use is a folder if we cannot access it though? Enter the `cd <folder>` command, standing for *change directory*. 

We may want to 'free' ourselves from our home directory and step to the root of the filesystem. This can be done with `cd /` to move to `/` folder, aka the root of the filesystem. 

## Manual
If you ever get confused on how a command works, `man <command>` is your friend! For example, say we forget what the function of `ls` was? We could find out quickly with `man ls`. Most UNIX commands have an associated manual entry, yet let it be noted that some may not. At that point, dare I say, Google is your friend.

## What's in this folder: 1
After creating files and folders for a while, it becomes hard to remember exactly what is in a folder! Use `ls` to return whatever is in your current folder, or `ls <folder>` to see what is in the supplied folder.

## Flags: What's in this folder: 2
Flags are an important part of UNIX commands. By


## The `alias` commmand 

## Whats going on?
-top, htop, kill

## `sudo`

## Vim vs Nano vs Emacs: The Eternal Battle

## IO

## Pipes

## Grep

## Connecting to other computers (SSH)

## Running programs

## Version control (Git)

## Installing More Programs

## Esoteric Additions
-fish 

## Final thoughts
Thanks for listening through this lecture! Whilst using the CLI may be frightening 
