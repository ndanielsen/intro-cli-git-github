# Introduction to the Command Line
This document outlines some basic commands for the Unix command line.  For Linux and OS X users, these should work in **Terminal**.  For Windows users, most of these will work in **Git SCM**.  
**Note**: Most of these commands will not work in the Windows Command Prompt.

### What is the command line?
The Command Line Interface (CLI) is a way of interacting with your computer based upon the text commands you type.  This is different from the way most people interact with their computers using their mouse and a Graphical User Interface (GUI).

### Why should I use it?
Once you become comfortable with the basics, it is a much more powerful way to use your computer.  You're able to do many things more quickly and programatically.  Also, you look cooler when using the command line.

### General Command Format
`<command> -<options> <arguments>`
* `<command>` is the actual command
* `<options>` (AKA “flags”) specify different ways of or options for executing the command
* `<arguments>` are things that go “into” the command to be operated on

### General Tips
* If there are spaces in file/folder names, use a “\” to “escape” the space characters or put the entire file path in quotes.
* Type the first few letters of the file or folder name, then hit tab to autocomplete the file or folder name.  This often auto-escapes spaces for you.
* Use the up and down arrow keys to navigate previously entered commands.

### Getting Help With a Command
For Linux/Mac users, the `man` command will give much more detailed information (a short **man**ual) about a command.  To use it type `man <command>` where `<command>` is any command line command.

`<command> --help` may also print out the "help" page about a particular command.

## File Paths
##### Relative File Paths
A relative file path specifies the path to a file taking into account what your current working directory is.  For example, if you were to give someone directions to your house, you would give the directions with context of leaving their house (the relative path from where they are to where you are).
##### Absolute File Paths
An absolute file path specifies the path to a file assuming there is no knowledge of what your current working directory is.  This means the file path starts at the root directory.  For example, if you were to give someone directions from their house to your house, you would start by telling them to be on earth, then go to your continent, then go to your country, then go to your region, etc.

## Basic Commands
##### `pwd`
* **P**rints **w**orking **d**irectory (the directory/folder you are currently in)
* Lets you see where you are in your file system
* Try it out; type `pwd` into your command line.
