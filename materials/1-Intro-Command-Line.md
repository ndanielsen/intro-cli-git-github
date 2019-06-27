# Introduction to the Command Line
This document outlines some basic commands for the Unix command line.

For Linux and OS X users, these should work in **Terminal**.  For Windows users, most of these will work in **Git Bash**.  
**Note**: Most of these commands will not work in the Windows Command Prompt.

### What is the command line?
The Command Line Interface (CLI) is a way of interacting with your computer based upon the text commands you type.  This is different from the way most people interact with their computers using their mouse and a Graphical User Interface (GUI).

### Why should I use it?
Once you become comfortable with the basics, it is a much more powerful way to use your computer.  You're able to do many things more quickly and programatically.  Also, you look cooler when using the command line.

### How do I open a command line terminal?

**Mac**: Click the Spotlight icon. It's the magnifying glass in the upper-right corner of the screen. In the search field, type in "Terminal."

**Windows**: After installing [git-scm](https://git-scm.com/), open `git bash` which should be findable in the explorer.

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

A path is the location of a file or directory on your computer. For example, the location of file on my computer is:

`/Users/ndanielsen/Projects/intro-cli-git-github/materials/1-Intro-Command-Line.md`


##### Absolute File Paths
An absolute file path specifies the path to a file assuming there is no knowledge of what your current working directory is.  This means the file path starts at the root directory.  For example, if you were to give someone directions from their house to your house, you would start by telling them to be on earth, then go to your continent, then go to your country, then go to your region, etc.

An example of an absolute path is the folder for this class. The absolute path is:

`/Users/ndanielsen/Projects/intro-cli-git-github`

##### Relative File Paths
A relative file path specifies the path to a file taking into account what your current working directory is.  For example, if you were giving directions to your office, you might say that your building is right across the street from the Chipotle and Bank of America on Flower St.

Given an absolute path of `/Users/ndanielsen/Projects/intro-cli-git-github`,

The current file path is a represented by `  .  `. For example, the path to a file in your current working directory is:

`./README.md`

From your current working director, the path to this `1-Intro-Command-Line.md` file from the `intro-cli-git-github` folder is:

`./materials/1-Intro-Command-Line.md`

The relative path to the another HackforLa project folder on my computer is:

`../ice-crea-shop`


## Basic Commands
##### `pwd`
* **P**rints **w**orking **d**irectory (the directory/folder you are currently in)
* Lets you see where you are in your file system
* Try it out; type `pwd` into your command line.

##### `ls`
* `ls` **l**i**s**ts files/folders in your current directory
* Can list files in a specific directory (file path) with `ls <file path>`
* Optional arguments
    * `ls -a` lists **a**ll files, including the hidden files
    * `ls -l` lists the files in a **l**ist with extra information
        * File permissions (owner, group, all users)
        * Number of links
        * Owner name
        * Owner group
        * File size
        * Created/Last modified date
        * File/Folder name
* `ls *` will list all files and the contents of all folders in your current working directory.

##### `clear`
* **Clear**s all output from your console

##### `history`
* Shows a history of previous commands that you have typed.
* You can also type !n to execute command number n.
* Use !! to execute the last command you typed.

##### `cd`
* `cd <path>` **c**hanges **d**irectory to the path you specify.  You can use a relative path or an absolute path.
* `cd ..` moves your working directory "up" one directory.
* `cd` moves your working directory to your "home" directory.
* Using `cd` and `ls` to navigate and look at your files at the command line is like clicking folders in Finder/Document Explorer.

##### `mkdir `
* `mkdir <name>` **m**a**k**es/creates a new **dir**ectory/folder named `<name>`.

##### `touch`
* `touch <file>` creates an empty file with the name `<file>`.
* This is useful for creating empty files to be edited at a later time.

##### `rm -i`
* `rm -i <file>` **r**e**m**oves a file.  The -i flag prompts you to confirm that you really want to delete the file.
* **NOTE**: Be careful with `rm`.  Once you `rm` a file, it is gone forever.  That's why it's smart to always use `rm -i`.
* `rm -ir <folder>` removes a folder and everything within it.
* **Note**: The `-r` option means **r**ecursive.  It's often needed for operations on a folder.

##### `mv`
* `mv <current file location> <new file location>` will **m**o**v**e a file from its `<current file location>` to a `<new file location>`. Don't forget the `/` if the `<new file location>` is a folder.
* This is the same as dragging and dropping a file from one place to another.
* `mv <current file name> <new file name>` renames a file by moving it.  You "move" it from one location, `<current file name>`, to another location, `<new file name>`, though it doesn't actually move locations.

##### `cp`
* `cp <current file location> <new file location>` will **c**o**p**y a file from its `<current file location>` to a `<new file location>`, leaving the original file untouched.  
* This is different from `mv` in that you are creating a new file and putting it somewhere rather than just moving the current file.

##### `zip`/`unzip` (Mac Users)
* `zip <zipped file> <original file>` will zip/compress the `<original file>` into a `<zipped file>`.
* `zip -r <zipped file> <original folder>` will zip/compress the `<original folder>` and all of its files into a `<zipped file>`.
* **Note**:  A list of files and folders, separated by spaces, can be zipped into one zipped file with `zip -r <zipped file> <original file 1> <original folder 2> ...`.
* `unzip <file>` will unzip/uncompress a file.

##### `gzip`/`gunzip` (Windows Users)
* `gzip <filename>` will compress the `<filename>` into `<filename>.gz`
* `gzip -r <original folder>` will compress all of the individual files of original folder
* `gunzip <filename>.gz` will uncompress the zipped file



## Exercise
* Create an empty directory called `test`.
* Change your working directory to this new `test` directory.
* Create *three* empty files in your `test` directory using `touch`.
* Remove *one* of the previously created files.
* Go up one directory and remove the `test` directory with the empty files in it.  **NOTE**:  Be careful and make sure you are removing the correct files!
* Create an empty file called `test.txt`.  
* Change the name to `opensource_is_cool.txt`.
* Create an empty file called `my_secrets.txt`.
* Create a new directory called `my_diary`.  
* Move the two previously created files into this directory.
* Create a new directory called `my_blog`.  Copy the file `opensource_is_cool.txt` from `my_diary` to `my_blog`.
* Examine the files in `my_blog` to confirm that `opensource_is_cool.txt` is there.
* Zip the folders `my_diary` and `my_blog` into a new file called `writings.zip`.
* Delete the folders `my_diary` and `my_blog`.
* Unzip `writings.zip` to get your folders back.
* Confirm that the two folders `my_diary` and `my_blog` have been recreated.
* Once you finish, you can delete everything:  `writings.zip`, `my_diary`, and `my_blog`.

## Advanced Command Line and Homework

In `4-Command-Line-Advanced.md`, I have provided more advanced command line exercises and a few exercises to test your knowledge!


## Resources
[Command Line Crash Course](https://learnpythonthehardway.org/book/appendixa.html)
A concise crash course for the CLI by the author of Learn Python the Hardway

[GNU Bash manual](https://www.gnu.org/software/bash/manual/)
Write simple yet powerful scripts using bash.

[Gawk: Effective AWK Programming](https://www.gnu.org/software/gawk/manual/)
Another language for writing powerful scripts using awk.
