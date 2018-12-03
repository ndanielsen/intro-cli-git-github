# Advanced Command Line
This document outlines more advanced commands for the Unix command line. At the end, there are advanced exercises that you can complete after the workshop.

## Advanced Commands

##### `find`
* `find <path to search> -name <name>` will search the specified path and **find** files and folders of the given `<name>`.
* If you want to search your current working diretory (`pwd`), you can use the `.` (a period) instead of a specifc path.  `.` means your current working directory.
* `<name>` can be the full name, but it can also be a partial match using wild card characters.
    * \* specifies any number of any characters
        * `find -name '*.csv'` will find all of the CSV files in your current directory.
    * ? specifies one character
        * `find -name '0?_submission.csv'` would find the following files in your current working directory:  `01_submission.csv`, `02_submission.csv`, and `03_submission.csv` but not `10_submission.csv`.
* This is a very useful and powerful command.

##### `head`
* `head <file>` prints the **head** (first ten lines) of the `<file>`.
* This is useful for looking at the beginning of a large file before performing a command on it.

##### `tail`
* `tail <file>` prints the **tail** (last ten lines) of the `<file>`.
* This is useful for looking at the end of a large file before performing a command on it.

##### `cat`
* `cat <file>` prints the entire `<file>`.
* This is useful sending the contents of the file into another command (more on that below).

##### `less`
* `less <file>` prints out enough of the file to fill up the console window and allows you to "scroll" through the file.
* Type `q` or `:q` to get out of the file and return to the command line.

##### `grep`
* `grep <pattern>` **g**lobally searches for a **r**egular **e**xpression and **p**rints the matches to the console.
* Works for partial matches
* Returns the line that matched.
* `grep <pattern> <file>` searches a `<file>` for the `<pattern>` and prints the matching lines to the console.
* If no file is given, `grep` will operate on the output from the previous command.

##### `wc`
* `wc <file>` returns the **c**ount of lines, **w**ords, and characters in a file.
* **Note**: A word is any set of characters delimited by space.
* If no file is given, `wc` will opearte on the output from the previous command.
* Combining `wc` and `grep` is a useful way of determining how many occurences of a specific word there are in a file.

##### `|`
* Let’s you **pipe** commands into each other
* `<command 1> | <command 2> | <command 3>` pipes these three commands into each other.  `<command 1>` completes and the results of it are piped into `<command 2>`.  `<command 2>` completes and the results of it are piped into `<command 3>`.  `<command 3>` completes and the results of it are printed to the console.
* This concept is a very powerful one on the command line.  This allows you to do complex things all from the command line.
* Many commands will use the output from a previous command as the input for the next command.

##### `>`
* `<command> > <file>` takes the output of the `<command>` and saves it in a `<file>`.
* This is useful for saving the results of a command to a file.

## Command Line Utilities

These might be helpful for you along your journey.

##### `sudo`
* `sudo <command>` runs the `<command>` with admin access.
* Stands for **S**uper **u**ser **d**o
* Use with caution as this gives your computer unrestricted access when performing the command that follows.  This is sometimes necessary to install software or access certain, restricted directories.

##### `nano`
* `nano <file>` will open the file in the NANO text editor.
* `Ctrl + X` will e**x**it the editor and prompt you to save the file or exit without saving.
* I would not recommend doing a lot of work in NANO, though it is useful to be aware of.

##### `vim`
* `vim <file>` will open the file in the VIM text editor.  But you can't start typing right away.
* Type `i` to enable **i**nsert mode and start typing.
* Use `:` to start a command
* `:w` to **w**rite/save a file
* `:x` to write/save the file you are working on and e**x**it the text editor
* `:q` to quit/exit the text editor.
* I would not recommend doing a lot of work in VIM, though it is useful to be aware of.

#### Part I
* Navigate to the directory where you cloned the `intro-cli-git-github` repository.
* Find all of the CSV files in the `data` directory.  How many are there?
* How many Markdown files are there in the `intro-cli-git-github` directory?
* How many lines are in the `ca_baby_names.csv` data?
* Using `ca_baby_names.csv`, return a list of the names from a '2017',. How many names are there in this list?  Write these names to a file called `2017_baby_names.csv`.
* Open the file `2017_baby_names.csv` to confirm it was correctly created.  Then, remove the file.
* Using `ca_baby_names.tsv`, how many baby names were in 1917?  Are there more baby names in 1917 than in 2017?

#### Part II
* Unzip `culture_centers.zip`
* Using grep, can you extract the email addresses from the unzipped file?
