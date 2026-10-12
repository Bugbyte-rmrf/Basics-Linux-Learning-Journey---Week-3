## Introduction

The practical module covered manage archive files at the command line, compressing files, archiving files, ZIP and UNZIP files.

The screenshots included in this README provide evidence of the commands I used and the results I obtained while completing the exercise.

---

### 1. Archiving and Compression

I learned the difference between **archiving** and **compression**: 
- *File archiving* -  When one or more files need to be transmitted or stored as efficiently as possible. 
- *Archiving* - Combines multiple files into a single archive. 
- *Compression* - Makes the files smaller by removing redundant information.
- *Un-archiving* - When an archive is decompressed, and one or more files are extracted.

#### Benefits of archiving and compression
When making a large number of files available, such as the source code to an application or a collection of documents, it is easier for people to download a compressed archive than it is to download files individually.
Log files have a habit of filling disks, so it is helpful to split them by date and compress older versions.
When backing up directories, it is easier to keep them all in one archive than it is to version (update) each file.
Some streaming devices such as tapes perform better if you’re sending a stream of data rather than individual files.
It can often be faster to compress a file before sending it to a tape drive or over a slower network and decompress it at the other end than it would be to send it uncompressed.

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
