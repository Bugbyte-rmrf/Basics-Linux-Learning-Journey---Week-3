## Introduction

The practical module covered manage archive files at the command line, compressing files, archiving files, ZIP and UNZIP files.

The screenshots included in this README provide evidence of the commands I used and the results I obtained while completing the exercise.

---

### 1. Introduction - Archiving and Compression

I learned the difference between **archiving** and **compression**: 
- *File archiving* -  When one or more files need to be transmitted or stored as efficiently as possible. 
- *Archiving* - Combines multiple files into a single archive. 
- *Compression* - Makes the files smaller by removing redundant information.
- *Un-archiving* - When an archive is decompressed, and one or more files are extracted.

### Benefits of archiving and compression
1. When making a large number of files available, such as the source code to an application or a collection of documents, it is easier for people to download a compressed archive than it is to download files individually.
2. Log files have a habit of filling disks, so it is helpful to split them by date and compress older versions.
3. When backing up directories, it is easier to keep them all in one archive than it is to version (update) each file.
4.Some streaming devices such as tapes perform better if you’re sending a stream of data rather than individual files.
5. It can often be faster to compress a file before sending it to a tape drive or over a slower network and decompress it at the other end than it would be to send it uncompressed.

### 1. Compression Files
**Compression algorithm** - A procedure the computer uses to encode the original file, and as a result, make it smaller.

I also learned about two types of compression:

- **Lossless compression** – No information is removed from the file. Compressing a file and decompressing it leaves something identical to the original.GIFs and PNGs are compressed but lossless. 
- **Lossy compression** – Information might be removed from the file. It is compressed in such a way that uncompressing a file will result in a file that is slightly different from the original.JPEGs use lossy compression

### Commands Used in Compressing Files
`gzip` command compress a file with the name of the file as the only argument. 
After that command completes, the original file is gone, and a compressed version with a file extension of .gz is left in its place.
Using `l` option with `gzip` command provides a reduction percentage



Compressed files can be restored to their original form using `gunzip` command or the `gzip –d` command. This process is called **decompression**. 


*Other Commmands Identical to `gzip` and `gunzip`
1.The `gzip` command uses the **Lempel-Ziv** data compression algorithm, while the `bzip` utilities use a different compression algorithm called **Burrows-Wheeler** block sorting, which can compress files smaller than `gzip` at the expense of more CPU time. These files can be recognized because they have a `.bz` or `.bz2` extension instead of a .gz extension.

2. The `xz` and `unxz` tools are functionally similar to `gzip` and `gunzip` in that they use the **Lempel-Ziv-Markov (LZMA)** chain algorithm, which can result in lower decompression CPU times that are on par with `gzip` while providing the better compression ratios typically associated with the `bzip2` tools. Files compressed with the `xz` command use the `.xz` extension.


bzip2 and bunzip2, as well as xz and unxz







### Evidence

**Screenshot 10 – Archiving and compression concepts**

*[Insert the relevant presentation screenshot here.]*

### What I Learned

Before this practical, I could easily think of archiving and compression as the same thing. I learned that they have different purposes: archiving is about combining files, while compression is about reducing their size.

With lossless compression, this multiple compression is not a problem, but if you compress and decompress a file several times using a lossy algorithm, you will eventually have something that is unrecognizable.


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
