# Basics-Linux-Learning-Journey---Week-3
My basic linux learning journey, hands-on practice, commands, concepts, and reflections.

## Introduction

This module exercise was focused on learning how to work with the Linux operating system through the Command Line Interface (CLI).

The main objective was to understand how the Linux filesystem is organized and how files, directories, and text can be managed using command-line commands. I worked through different Linux commands and observed their output directly in the terminal.

The practical covered managing files and directories, copying files and directories, moving files, renaming files, creating files, removing files, removing directories and creating directories

filesystem navigation, file and directory management, file viewing, archiving and compression, sorting and filtering information, input/output redirection, pipes, and regular expressions.

The screenshots included in this README provide evidence of the commands I used and the results I obtained while completing the exercise.

---

# 6. Globbing and Wildcards

I learned about globbing, which allows patterns to be used when specifying filenames.

The following wildcard characters:

```text
*
?
[ ]
!
```

The asterisk `*` represents zero or more characters.

The question mark `?` represents exactly one character.

Square brackets `[ ]` can represent a range or list of characters.

The exclamation mark `!` can be used with square brackets to negate a range.

### Evidence

**Screenshot 6 – Globbing and wildcard characters**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that I do not always need to specify every filename individually. Wildcards allow patterns to be used to work with groups of filenames.

---

# 7. Copying Files and Directories

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

# 8. Moving, Renaming, Creating and Removing Files

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

# 9. Creating and Removing Directories

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


---

# 10. Archiving and Compression

I learned the difference between **archiving** and **compression**.

Archiving combines multiple files into a single archive. Compression reduces the size of information by removing redundant information.

I also learned about two types of compression:

- **Lossless compression** – information is not removed and the original data can be recovered exactly.
- **Lossy compression** – some information is removed, which can result in a smaller file.

### Evidence

**Screenshot 10 – Archiving and compression concepts**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

Before this practical, I could easily think of archiving and compression as the same thing. I learned that they have different purposes: archiving is about combining files, while compression is about reducing their size.

---

# 11. gzip and gunzip

I learned about gzip compression.

`gzip` compresses a file and produces a `.gz` file.

`gunzip` is used to decompress a compressed file and restore it.

### Evidence

**Screenshot 11 – gzip and gunzip**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that Linux provides command-line tools for reducing file sizes and restoring compressed files.

---

# 12. tar Archives

I learned how the `tar` command is used to create, list, and extract archives.

The three main modes covered were:

### Create

```bash
tar -c
```

Creates an archive.

### List

```bash
tar -t
```

Displays the contents of an archive without extracting it.

### Extract

```bash
tar -x
```

Extracts files from an archive.

### Evidence

**Screenshot 12 – tar command**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that `tar` is useful for combining multiple files into a single archive that can later be opened and separated back into its original files.

---

# 13. ZIP and UNZIP

I also learned about ZIP files.

```bash
zip
```

is used to add files to an archive and compress them.

```bash
zip -r
```

allows directories and their contents to be included recursively.

To extract an archive:

```bash
unzip
```

To list the contents without extracting:

```bash
unzip -l
```

### Evidence

**Screenshot 13 – ZIP and UNZIP commands**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned another method of creating compressed archives and how to inspect and extract their contents.

---

# 14. Viewing Files with cat

I learned how to display the contents of text files using:

```bash
cat filename
```

`cat` stands for concatenate and can be used to display and combine text.

### Evidence

**Screenshot 14 – cat command**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that I can quickly inspect the contents of a text file directly from the terminal without opening a graphical text editor.

---

# 15. Viewing Large Files with Pagers

For larger files, I learned about pager commands.

The presentation covered:

```bash
less
```

and:

```bash
more
```

`less` allows information to be viewed one screen at a time.

Some of the navigation keys I learned include:

- `Spacebar` – move forward
- `b` – move backward
- `Enter` – move forward one line
- `q` – quit

I also learned that `/` can be used to search forward and `?` can be used to search backward.

### Evidence

**Screenshot 15 – Pager commands**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that I do not have to display an entire large file at once. A pager allows me to move through the information gradually and search within it.

---

# 16. head and tail

I learned that `head` and `tail` can be used to display only part of a file.

`head` displays the first lines of a file.

`tail` displays the last lines.

### Evidence

**Screenshot 16 – head and tail**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

These commands are useful when I only need to inspect the beginning or end of a file instead of viewing everything.

---

# 17. Pipes

I learned about the pipe character:

```text
|
```

A pipe sends the output of one command to another command.

For example, the output of one command can be passed to `sort` or another filtering command.

### Evidence

**Screenshot 17 – Pipe command**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

The pipe was an important concept because it showed me that Linux commands can be combined. One command does not have to perform the entire task by itself.

---

# 18. Input and Output Redirection

I learned about Linux's three standard streams:

### STDIN

Standard input is information entered into a command, usually from the keyboard.

### STDOUT

Standard output is the normal output produced by a command.

### STDERR

Standard error contains error messages produced by commands.

I also learned that Linux provides input/output redirection, which allows command information to be passed to different streams.

### Evidence

**Screenshot 18 – Input/output redirection**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that commands have different forms of input and output and that Linux provides mechanisms for controlling where that information goes.

---

# 19. Sorting Input with sort

I learned that `sort` can rearrange lines according to their contents.

The presentation covered:

```text
-t
-k
-n
```

`-t` specifies the field delimiter.

`-k` identifies the field to sort by.

`-n` performs a numeric sort.

### Evidence

**Screenshot 19 – sort command**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that sorting can be performed in different ways depending on how the data is structured. This is especially useful when working with files containing multiple fields.

---

# 20. File Statistics with wc

I learned that `wc` provides information about files, including the number of lines, words and bytes.

### Evidence

**Screenshot 20 – wc command**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that `wc` provides a quick way to obtain basic statistics about the contents of a file instead of manually counting them.

---

# 21. Filtering File Sections with cut

I learned that `cut` is used to extract specific sections or fields from text.

The presentation covered:

```text
-d
-f
```

The `-d` option specifies the delimiter.

The `-f` option specifies which fields should be displayed.

### Evidence

**Screenshot 21 – cut command**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that `cut` is useful for working with structured text where information is separated into fields.

---

# 22. Filtering File Contents with grep

I learned that `grep` searches for lines that match a particular pattern.

Some of the options covered were:

```text
--color
-c
-v
-i
-w
```

`--color` highlights matching items.

`-c` counts matching lines.

`-v` reverses the search and displays lines that do not match.

`-i` ignores capitalization.

`-w` searches for whole-word matches.

### Evidence

**Screenshot 22 – grep command and output**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that `grep` is useful for quickly finding specific information in a file or in the output of another command. Its options allow the search to be made more specific.

---

# 23. Regular Expressions

I learned about regular expressions as a way of searching for patterns rather than only exact text.

The basic regular expression characters covered were:

```text
.
[ ]
*
^
$
\
```

The period `.` can match any character except a newline.

Square brackets can match a character from a list or range.

The asterisk `*` represents zero or more occurrences of a character or pattern.

The caret `^` is used to match the beginning of a line.

The dollar sign `$` is used to match the end of a line.

The backslash `\` can be used when a special character needs to be matched literally.

### Evidence

**Screenshot 23 – Basic regular expressions**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

Regular expressions showed me that searching can be based on patterns. This is more flexible than searching for one exact word or character sequence.

---

# 24. Extended Regular Expressions

I also learned about extended regular expressions.

The presentation covered:

```text
?
+
|
```

The question mark can indicate that the previous character is optional.

The plus sign indicates one or more occurrences.

The vertical bar provides alternatives, similar to an "OR".

Extended regular expressions require an appropriate option for the command to recognize them.

### Evidence

**Screenshot 24 – Extended regular expressions**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

I learned that regular expressions can be extended to create more flexible patterns. This makes it possible to perform more advanced searches.

---

# 25. Challenges I Encountered

One of the main challenges during the practical was becoming comfortable with the Linux command line. Unlike a graphical interface, the terminal requires commands to be entered correctly, and I had to pay attention to my current location in the filesystem.

Another challenge was remembering the different command options. Many commands perform a basic task, but options such as `-a`, `-l`, `-r`, `-i`, `-n`, and others change how the command behaves.

I also found that commands become more powerful when they are combined. Understanding pipes, filtering, sorting, and redirection required me to think about how the output of one command can become the input of another.

Regular expressions were another challenging concept because the symbols have specific meanings. I had to understand that characters such as `*`, `^`, `$`, and `[]` can represent patterns rather than simply being ordinary characters.

The practical nature of the work helped me overcome these challenges because I was able to run the commands myself and observe the results.

---

# 26. What I Learned Overall

The practical gave me a better understanding of how Linux works from the command line.

The main concepts I learned were:

- Linux uses a hierarchical filesystem beginning at `/`.
- `~` represents the user's home directory.
- `pwd`, `ls`, and `cd` are fundamental navigation commands.
- Absolute and relative paths identify locations in different ways.
- `ls` has several options for obtaining different types of information.
- Wildcards can be used to match filename patterns.
- `cp`, `mv`, `touch`, and `rm` are used to manage files.
- `mkdir` and `rmdir` are used to manage directories.
- Archiving and compression are different concepts.
- `gzip`, `gunzip`, `tar`, `zip`, and `unzip` can be used to manage archives and compressed files.
- `cat`, `less`, and `more` provide ways of viewing files.
- `head` and `tail` allow selected parts of files to be viewed.
- Pipes allow commands to be connected together.
- Linux uses STDIN, STDOUT, and STDERR for input and output.
- `sort` can organize information.
- `wc` provides file statistics.
- `cut` extracts selected fields.
- `grep` searches and filters information.
- Regular expressions provide pattern-based searching.

---

# 27. Key Takeaways

My biggest takeaway from this practical is that the Linux command line is much more than a way of opening files or running individual commands. Commands can be combined and modified with options to perform more specific tasks.

I also learned that understanding the filesystem is essential. Before performing an operation, I need to know where I am, what files are available, and what the command is going to do.

Another important takeaway was the importance of understanding command output. Running a command and looking at its result helped me understand what the command was actually doing instead of simply memorizing its definition.

Finally, I learned that many Linux commands are designed to work together. Pipes, filtering, sorting, and regular expressions make it possible to process information efficiently from the terminal.

---

# 28. Conclusion

This practical helped me develop a stronger understanding of Linux and the Command Line Interface.

Through hands-on practice, I learned how to navigate the Linux filesystem, manage files and directories, work with paths, create and manage archives, view and process text files, sort and filter information, and use regular expressions.

The screenshots included throughout this README show the commands I worked with and the results produced in the terminal. They provide evidence that the concepts were explored through practical work rather than only through theory.

The most valuable part of the practical was being able to run the commands myself and see how they behaved. This helped me understand both the purpose of individual commands and how different commands can be combined to accomplish more complex tasks.

Overall, I now have a better understanding of Linux command-line operations and greater confidence in using the terminal to work with files, directories, and text.
