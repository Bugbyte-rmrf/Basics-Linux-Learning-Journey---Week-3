## Introduction

This module exercise covered managing files and directories, copying files and directories, moving files, renaming files, creating files, removing files, removing directories and creating directories

The screenshots included in this README provide evidence of the commands I used and the results I obtained while completing the exercise.

---

###1. Globbing

I learned that **Glob characters** are often referred to as **wild cards**. These are symbol characters that have special meaning to the shell.

Globs are powerful because they specify patterns that match filenames in a directory. So instead of manipulating a single file at a time, one can easily execute commands that affect many files. 

The following are wildcard characters:

```text
*
?
[ ]
!
```

### 1. Asterisk *

The asterisk `*` represents zero or more of any character in a filename.




The question mark `?` represents exactly one character.

Square brackets `[ ]` can represent a range or list of characters.

The exclamation mark `!` can be used with square brackets to negate a range.

### Evidence

**Screenshot 6 – Globbing and wildcard characters**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that I do not always need to specify every filename individually. Wildcards allow patterns to be used to work with groups of filenames.

---

### 2. Copying Files and Directories

I learned how to copy files using the `cp` command.

```bash
cp source destination
```

The source is the file being copied and the destination specifies where the copy should go.

I also learned about the following options:

```bash
cp -v source destination
```

The `-v` option produces verbose output.

For directories:

```bash
cp -r source_directory destination_directory
```

The `-r` option allows directories and their contents to be copied recursively.

The presentation also covered:

```text
-i
-n
```

The `-i` option prompts before overwriting, while `-n` prevents overwriting an existing destination.

### Evidence

**Screenshot 7 – Copying files and directories**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned how to make copies of files and directories and how options can make the operation safer by preventing accidental overwriting.

---

### 3. Moving, Renaming, Creating and Removing Files

I learned several commands for managing files.

### `mv`

```bash
mv source destination
```

The `mv` command moves a file. It can also be used to rename a file.

### `touch`

```bash
touch filename
```

The `touch` command is used to create a file.

### `rm`

```bash
rm filename
```

The `rm` command removes a file.

### Evidence

**Screenshot 8 – File management commands**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that many normal file-management tasks can be performed directly from the terminal. I also learned that commands such as `rm` need to be used carefully because they remove files.

---

### 4. Creating and Removing Directories

I learned how to create and remove directories.

### Creating a directory

```bash
mkdir directory_name
```

The `mkdir` command creates a directory.

### Removing an empty directory

```bash
rmdir directory_name
```

The `rmdir` command removes an empty directory.

### Removing a directory recursively

```bash
rm -r directory_name
```

The `-r` option allows `rm` to remove directories and their contents recursively.

### Evidence

**Screenshot 9 – Creating and removing directories**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that files and directories have different commands and options for managing them. I also learned that recursive operations need to be used carefully because they can affect everything inside a directory.
