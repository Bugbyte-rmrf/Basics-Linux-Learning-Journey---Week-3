## Introduction

This module exercise was focused on learning how to work with the Linux operating system through the Command Line Interface (CLI).

The main objective was to understand how the Linux filesystem is organized and how files, directories, and text can be managed using command-line commands. I worked through different Linux commands and observed their output directly in the terminal.

The screenshots included in this README provide evidence of the commands I used and the results I obtained while completing the exercise.

---

### 1. Linux File System and Directory Structure

I learned that Linux organizes its files in a single hierarchical filesystem. Unlike Windows, which commonly uses drive letters such as `C:` or `D:`, Linux starts from a root directory represented by `/`.

I also learned that the tilde character `~` is a shortcut representing the current user's home directory.

This gave me a basic understanding of how Linux organizes files and how I should think about locations when working from the terminal.

---

### 2. Terminal Navigation

I learned the basic commands used to navigate through the Linux filesystem:

```bash
ls
```

The `ls` command displays the contents of a directory.

```bash
pwd
```

The `pwd` command displays the exact path of my current working directory.

```bash
cd
```

The `cd` command is used to change directories. When used without an argument, it takes me back to my home directory.

### What I Learned - Terminal Navigation

I learned that navigation in Linux depends on understanding where I currently am in the filesystem. `pwd` helps me confirm my location, `ls` lets me see what is available, and `cd` allows me to move between locations.

If the user tries to change to a directory that does not exist, the command returns an error message

### Evidence - Terminal Navigation

<img width="613" height="110" alt="Screenshot from 2026-10-05 18-30-29" src="https://github.com/user-attachments/assets/1a15decd-9148-4138-b4a6-b3190f537e83" /> 

---

### 3. Shortcuts

I also learned the following characters: 

```text
..
```

Regardless of which directory the user is in, the two period `..` characters always represents one directory higher relative to the current directory, sometimes referred to as the parent directory. 

```text
.
```

Regardless of which directory the user is in, the single period `.` character always represents the current directory.

### Evidence - Shortcuts

<img width="615" height="71" alt="Screenshot from 2026-10-05 20-01-13" src="https://github.com/user-attachments/assets/6e637bc7-81b2-4766-970d-44e668765ca9" />

---

### 3. Absolute and Relative Paths

I learned about two ways of identifying locations in the Linux filesystem:

a) An **absolute path** specifies the complete location and starts from the root directory `/`.

```text
cd /home/sysadmin
```

b) A **relative path** starts from my current working directory rather than from the root. The simplest method is to use a single relative path that covers the journey from the origin to the destination directory.

```text
/home/sysadmin
```

### What I Learned - Absolute and Relative Paths

The difference between absolute and relative paths is important because a relative path depends on my current location, while an absolute path identifies the location independently of where I currently am.

This helped me understand why knowing my current directory is important when using the terminal.

### Evidence -  Absolute and Relative Paths

*<img width="614" height="85" alt="Screenshot from 2026-10-05 18-44-54" src="https://github.com/user-attachments/assets/3ea00a79-144f-4d0a-b2f7-23ea5b90fc60" />*

---

### 4. Listing Files and Directories

The `ls` command has several options that provide different information:

```bash
ls -a
```
<img width="644" height="84" alt="Screenshot from 2026-10-05 20-50-26" src="https://github.com/user-attachments/assets/cb870c0d-473c-4e63-9b38-b7789e208b8a" />

*What it does:* Displays all files, including hidden files.

```bash
ls -l
```
<img width="493" height="49" alt="ls-l" src="https://github.com/user-attachments/assets/48666e45-c9d1-4e3b-8660-b65d3ee3c1cc" />

*What it does:* Displays a long-format listing containing information such as: 
- file type,
- permissions,
- hard link count,
- ownership,
- file size,
- timestamp and
- file name.

```bash
ls -lh
```

<img width="513" height="33" alt="ls -lh" src="https://github.com/user-attachments/assets/b30babc2-370a-4564-8417-b12d513829d5" />

*What it does:* Displays file sizes in a human-readable format such as megabytes or gigabytes.

```bash
ls -ld
```

<img width="618" height="78" alt="Screenshot from 2026-10-05 20-59-02" src="https://github.com/user-attachments/assets/180ed481-16b5-4bbd-a059-ba77365f5b24" />

*What it does:* When the `-d` option is used, it refers to the current directory, and not the contents within it. When `ls -ld`, the command lists the directory itself rather than its contents.

```bash
ls -R
```

*What it does:* Performs a recursive listing, showing all of the files in directory and its subdirectories.

<img width="614" height="167" alt="Screenshot from 2026-10-05 21-03-00" src="https://github.com/user-attachments/assets/21fcf4ac-f35a-4444-a863-ee1114363c72" />

### What I Learned - Listing Files and Directories

I learned that commands can be modified using options to change what they display or how they operate. Instead of only using `ls` to see filenames, I can use different options to obtain more detailed information.

I also learnt that it is important to be careful with the command `ls -R` . Running the command on the root directory would list every file on the file system, including all files on any attached USB device and DVD in the system.  Therefore limit the use of recursive listings to smaller directory structures.

---

### 5. Sorting Directory Listings

I learned that the output of `ls` can be sorted using different options:

`-S` It can be used to sorts by file size, lists files from the largest (when used with `-l` option) and display human-readable file sizes when used with `-h` option.

<img width="615" height="222" alt="Screenshot from 2026-10-05 21-14-13" src="https://github.com/user-attachments/assets/3dc83ec6-c20c-429a-8efb-7a30bb4aa97a" />

`-t` .It sorts according to modification time listing most recently modified files first. For more detailed modification time information, use the `--full-time` option to display the complete timestamp (including hours, minutes, seconds).

<img width="619" height="329" alt="Screenshot from 2026-10-05 21-33-17" src="https://github.com/user-attachments/assets/c12c6ab2-5059-403b-b27e-407317427d2f" />

`-r` . It reverses the sorting order. When combined with `-S`, the command will sort files by size, smallest to largest.

<img width="620" height="220" alt="Screenshot from 2026-10-05 21-40-58" src="https://github.com/user-attachments/assets/1d034b34-50ae-4dd1-ba64-ee03a903dcde" />

When the `r` command uses `-t options` ,it list files by modification date, oldest to newest.

<img width="644" height="235" alt="Screenshot from 2026-10-05 21-42-29" src="https://github.com/user-attachments/assets/f68ca555-aa2c-4897-8c5e-b511ea07aafa" />

### What I Learned - Sorting Directory Listings

I learned that sorting options are useful when I need to find particular files quickly, such as the largest files or the files that were modified most recently.
