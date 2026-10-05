## Introduction

This module exercise covered managing files and directories, copying files and directories, moving files, renaming files, creating files, removing files, removing directories and creating directories

The screenshots included in this README provide evidence of the commands I used and the results I obtained while completing the exercise.

---

### 1. Globbing

I learned that **Glob characters** are often referred to as **wild cards**. These are symbol characters that have special meaning to the shell.

Globs are powerful because they specify patterns that match filenames in a directory. So instead of manipulating a single file at a time, one can easily execute commands that affect many files. 

The following are wildcard characters:

```text
*
?
[ ]
!
```

### 1.1 Asterisk *

The asterisk `*` represents zero or more of any character in a filename.

<img width="650" height="41" alt="Screenshot from 2026-10-05 22-34-51" src="https://github.com/user-attachments/assets/f006535f-effb-4d09-89b0-86d3b5981834" />

The pattern `t*` matches any file in the /etc directory that begins with the character t followed by zero or more of any character. In other words, any files that begin with the letter t.

### 1.2 Question mark ?

The question mark `?` represents exactly one character.

<img width="650" height="41" alt="Screenshot from 2026-10-05 22-35-37" src="https://github.com/user-attachments/assets/a505593a-511e-4106-91f0-02d3890de1a5" />

It display all of the files in the /etc directory that begin with the letter t and have exactly 7 characters after the `t` character.

### 1.3 Square brackets [ ]

Square brackets `[ ]`  are used to match a single character by representing a range of characters that are possible match characters.

<img width="650" height="79" alt="Screenshot from 2026-10-05 22-42-34" src="https://github.com/user-attachments/assets/50b27deb-6289-43a1-8e99-ed40a395ba89" />

*The above example*: the `/etc/[gu]*` pattern matches any file that begins with either a g or u character and contains zero or more additional characters:

Brackets can also be used to a represent a range of characters. 

<img width="617" height="134" alt="Screenshot from 2026-10-05 22-44-45" src="https://github.com/user-attachments/assets/26b870cf-1133-4f25-bb40-9177c22b1d16" />

*The above example*: `/etc/[a-d]*` pattern matches all files that begin with any letter between and including a and d

Brackets also displays any file that contains at least one number:

<img width="613" height="61" alt="Screenshot from 2026-10-05 22-45-04" src="https://github.com/user-attachments/assets/6cb76283-abe7-43ff-ac54-270ac7fdee01" />

*The above example*: `/etc/*[0-9]*` pattern displays any file that contains at least one number:

### 1.4 Exclamation mark !

The exclamation mark `!` can be used with square brackets to negate a range.

<img width="616" height="57" alt="Screenshot from 2026-10-05 22-49-39" src="https://github.com/user-attachments/assets/a99854d8-1fb0-4dc2-a777-e9004e2d9524" />

*The above example*: `/etc/[!DP]*` matches any file that does not begin with a D or P.

### What I Learned - Globbing

I learned that I do not always need to specify every filename individually. Wildcards allow patterns to be used to work with groups of filenames.

---

### 2. Copying Files

I learned how to copy files using the `cp` command. The structure of the command is:
```bash
cp source destination
```

The `source` is the file being copied and the `destination` specifies where the copy is to be located. 

<img width="613" height="79" alt="Screenshot from 2026-10-05 23-07-16" src="https://github.com/user-attachments/assets/6d34c15e-d81f-4af6-b448-3970b8b18c32" />

*What it means*: Copies the /etc/hosts file to home directory. The `~` character represents home directory.

### 2.1 Verbose Mode 

I also learned `-v` option stands for verbose. It auses the cp command to produce output if successful.

<img width="616" height="57" alt="Screenshot from 2026-10-05 22-49-39" src="https://github.com/user-attachments/assets/e17d37f5-09d2-47ee-81cd-7ab342b7e9e0" />

To give the new file a different name, provide the new name as part of the destination.

<img width="613" height="79" alt="Screenshot from 2026-10-05 23-07-16" src="https://github.com/user-attachments/assets/9acd5b7d-270e-459c-a4c5-1e1c3312c57a" />

---

### 3. Avoid Overwriting Data

I learned that where the destination file exists, the `cp` command overwrites the existing file's contents with the contents of the source file.

### 3.1 Illustrated Overwritten Data

<img width="611" height="118" alt="Screenshot from 2026-10-05 23-21-48" src="https://github.com/user-attachments/assets/8977245c-40bf-416a-bae5-f837f575370b" />

*The above example* - It illustrates the overwriting problem:
- New file is created in the home directory by copying an existing file
- View the information about the file with `ls` command
- View the contents of the file using the `cat` command
- the `cp` command destroys the original contents of the example.txt file

### 3.2 Results - Overwritten Data

After the `cp` command is complete, the size of the file has changed and the contents are different.

<img width="613" height="78" alt="Screenshot from 2026-10-05 23-29-37" src="https://github.com/user-attachments/assets/bc33f58c-1a25-4e55-9e3b-d7842a1d48df" />

### 3.3 Safeguards Against Overwrites
`-i` *interactive* option, the `cp` command prompts the user before overwriting a file. The `-i` option requires you to answer y or n for every copy that could end up overwriting an existing file's contents. 

<img width="642" height="135" alt="Screenshot from 2026-10-05 23-36-28" src="https://github.com/user-attachments/assets/9d8a3b22-0ff4-4d5c-bceb-c7304d3dba39" />

To answer n to each prompt automatically, use the `-n` option. It stands for no clobber, or no overwrite.

<img width="642" height="135" alt="Screenshot from 2026-10-05 23-36-28" src="https://github.com/user-attachments/assets/12ab5c92-e4cb-4b7e-ae3f-c8a5a1d553e1" />

### 4. Copying Directories

I learned that the recursive `-r` option allows the `cp` command to copy both files and directories. The structure is:
```bash
cp -r source_directory destination_directory
```

### What I Learned

I learned how to make copies of files and directories and how options can make the operation safer by preventing accidental overwriting.

I also learned that the the recursive `-r` option allows the cp command can copy the entire directory structure which could result in copying a lot of files and directories!

---

### 5. Moving and Renaming Files

I learned several commands for managing files.

*Moving Files* : The `mv` command moves a file.  The syntax is:
```bash
mv source destination
```

<img width="620" height="164" alt="Screenshot from 2026-10-05 23-49-34" src="https://github.com/user-attachments/assets/515978c5-e329-44d2-9d2f-c49f99a1abed" />

*Renaming Files* : The `mv` command rename a file. If the destination for the `mv` command is a directory, the file is moved to the directory specified. The name of the file only changes if a destination file name is also specified.

<img width="620" height="164" alt="Screenshot from 2026-10-05 23-53-42" src="https://github.com/user-attachments/assets/eb828623-d5b8-4dbc-be6d-9f9ab662357d" />

I also learned that when using `mv` command, if a destination directory is not specified, the file is renamed using the destination file name and remains in the source directory. 

<img width="610" height="113" alt="Screenshot from 2026-10-05 23-58-08" src="https://github.com/user-attachments/assets/61a0b48f-98da-487a-b983-dc6fb6383588" />

*Additional Move Options* : the `mv` command provides the following options:
-`i` - Interactive: Ask if a file is to be overwritten.
-`n` -	No Clobber: Do not overwrite a destination file's contents.
-`v` - Verbose: Show the resulting move.

### 6. Creating and Removing Files
I learned that the `touch` command is used to create a file.

<img width="608" height="61" alt="Screenshot from 2026-10-06 00-05-18" src="https://github.com/user-attachments/assets/f7524474-3985-4d0c-b396-05eb87e4cef3" />

I also learned that the `rm` command is used to delete a file.As a precaution, it is important to use the `-i` option when deleting multiple files.

<img width="611" height="202" alt="Screenshot from 2026-10-06 00-09-51" src="https://github.com/user-attachments/assets/e7aa8754-3990-4b60-bdda-984bf38df4ab" />

### 6. Removing Directories



```



### `rm`

```bash
rm filename
```

The `rm` command removes a file.

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


### What I Learned

I learned that files and directories have different commands and options for managing them. I also learned that recursive operations need to be used carefully because they can affect everything inside a directory.
