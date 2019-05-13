# How to use the terminal
The terminal is a computer interface that uses the command line rather than a graphical interface to execute commands.

## List Files

The `ls` command lists all files in a directory. For an exhaustive look at every available option for `ls`, check out the [manpage](http://man7.org/linux/man-pages/man1/ls.1.html).

`ls`

### Common Flags
Flags can be invoked with the `-` character and the desired flags.

The `a` flag shows all files in the directory, including hidden files. Filenames starting with a dot are considered hidden. 

```
$ ls
README.md
git.md
terminal.md

$ ls -a
.
..
.git
README.md
git.md
terminal.md

```

The `l` flag includes file details.

```
$ ls -l
total 24
-rw-r--r--@ 1 kaizensoze  wheel   274 May 13 11:40 README.md
-rw-r--r--@ 1 kaizensoze  wheel  3433 May 13 11:44 git.md
-rw-r--r--@ 1 kaizensoze  wheel  3812 May 13 11:50 terminal.md
```

The `r` flag reverses the order of listed files.

```
$ ls -r
terminal.md
git.md
README.md
```

Flags can be combined.

```
$ ls -la
total 24
drwxr-xr-x   6 kaizensoze  wheel   192 May 13 11:41 .
drwxr-xr-x   4 kaizensoze  wheel   128 May 13 11:07 ..
drwxr-xr-x  13 kaizensoze  wheel   416 May 13 11:40 .git
-rw-r--r--@  1 kaizensoze  wheel   274 May 13 11:40 README.md
-rw-r--r--@  1 kaizensoze  wheel  3433 May 13 11:44 git.md
-rw-r--r--@  1 kaizensoze  wheel  3812 May 13 11:50 terminal.md
```

## Navigating Directories

To change directories on the command line, use the `cd` command.

### Syntax
`cd <directoryName>`

This command will move you to the directory you specify. The directory must be available in your current location, or referenced with an absolute path.

If you have a directory inside your current directory called `images`, you would navigate to it with: `cd images`

You can auto-complete a directory name by pressing the `TAB` key.

### Move to the top-level directory
`cd /`

### Move to the logged-in user's home directory
`cd ~`

### Move up one level
`cd ..`

### Move up two levels
`cd ../..`

## Create a directory

The `mkdir` command creates a directory inside your current directory.

## Copy a file

The `cp` command create a duplicate of the file you specify at the location you specify.

### Syntax
`cp <file1 location> <file2 location>`

To copy a file named `myfile.txt` to `myduplicate.txt` you would run `cp myfile.txt myduplicate.txt`

You can copy files to other directories.

`cp myfile.txt ~/myHomeDirectoryFile.txt`

You can copy entire folders.

`cp <folder> <duplicateFolder>`

## Move a file
The syntax to move a file is exactly the same as the command to copy. Rather than creating a duplicate, the file is removed from its original location and created in the new location.

### Syntax
`mv <original file location> <new file location>`

### Rename a file
`mv myFile.txt newFilename.txt`

### Move a file to another folder
`mv myfile.txt ~/myHomeFile.txt`

### Move an entire folder
`mv <folder> <new folder location>`

## Create an empty file
An empty file can be created with the `touch` command.

### Syntax
`touch <filename>`

### Create an empty file in a subdirectory
`touch myFolder/emptyfile.txt`

### Create an empty file in a specific location
`touch ~/git_projects/new.html`

## Display the contents of a file in the terminal
The `cat` command is used to output the contents of a file to a terminal.

### Syntax
`cat <filename>`

## Delete a file
To delete a file, use the `rm` command. This is an extremely powerful utility and should not be used unless you know exactly what you're doing.

**Once a file or folder is deleted, it cannot be recovered. It is PERMANENT.**

## Syntax
`rm <filename>`