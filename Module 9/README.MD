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

### 2. Compression Files
**Compression algorithm** - A procedure the computer uses to encode the original file, and as a result, make it smaller.

I also learned about two types of compression:

- **Lossless compression** – No information is removed from the file. Compressing a file and decompressing it leaves something identical to the original.GIFs and PNGs are compressed but lossless. 
- **Lossy compression** – Information might be removed from the file. It is compressed in such a way that uncompressing a file will result in a file that is slightly different from the original.JPEGs use lossy compression

### Commands Used in Compressing Files
`gzip` command compress a file with the name of the file as the only argument. 
After that command completes, the original file is gone, and a compressed version with a file extension of .gz is left in its place.
Using `l` option with `gzip` command provides a reduction percentage. 

<img width="643" height="172" alt="Image" src="https://github.com/user-attachments/assets/111c6941-26d3-4f46-a849-bd1f5f76007d" />

Compressed files can be restored to their original form using `gunzip` command or the `gzip –d` command. This process is called **decompression**. 

<img width="613" height="55" alt="Image" src="https://github.com/user-attachments/assets/70775100-78c2-4228-902a-e3158fdf29fd" />

### Other Commmands Identical to `gzip` and `gunzip`

1. The `gzip` command uses the **Lempel-Ziv** data compression algorithm, while the `bzip` utilities use a different compression algorithm called **Burrows-Wheeler** block sorting, which can compress files smaller than `gzip` at the expense of more CPU time. These files can be recognized because they have a `.bz` or `.bz2` extension instead of a .gz extension.

2. The `xz` and `unxz` tools are functionally similar to `gzip` and `gunzip` in that they use the **Lempel-Ziv-Markov (LZMA)** chain algorithm, which can result in lower decompression CPU times that are on par with `gzip` while providing the better compression ratios typically associated with the `bzip2` tools. Files compressed with the `xz` command use the `.xz` extension.

### What I Learned
Compressing an already compressed file will not make it smaller. This fact is often forgotten when it comes to images since they are already stored in a compressed format.

With lossless compression, this multiple compression is not a problem, but if you compress and decompress a file several times using a lossy algorithm, you will eventually have something that is unrecognizable.

---

### 3. Archiving Files
The traditional UNIX utility to archive files is called `tar`, which is a short form of **TApe aRchive**. 

I learned that it was used to stream many files to a tape for backups or file transfer. 

The `tar` command takes in several files and creates a single output file that can be split up again into the original files on the other end of the transmission.

### Modes under `tar` Command
**1. Create Mode**

I learned that the Create mode make a new archive out of a series of files.

Creating an archive with the `tar` command requires two named options: `tar -c [-f ARCHIVE] [OPTIONS] [FILE...]`

- `-c` - Create an archive.
- `-f ARCHIVE` - Use archive file. The argument `ARCHIVE` will be the name of the resulting archive file.

<img width="516" height="47" alt="Image" src="https://github.com/user-attachments/assets/f54e7ba4-3826-49e1-b267-7af9120f4ba9" />

**Commands Used in Create Mode**
 I learned that tarballs can be compressed for easier transport, either by using `gzip` on the archive or by having `tar` do it with the `-z` option.

`z` compress (or decompress) an archive using the gzip command.

<img width="516" height="47" alt="Image" src="https://github.com/user-attachments/assets/1435461b-38f6-4951-a96e-140b0f416b92" />

The output is much smaller than the tarball itself, and the resulting file is compatible with `gzip`, which can be used to view the compression details. 

<img width="516" height="47" alt="Image" src="https://github.com/user-attachments/assets/58097a5c-7449-4a8b-9a31-8a282237bf12" />

I also learned that `bzip2` compression can be used instead of `gzip `by substituting the `-j` option for the `-z` option and using `.tar.bz2`, `.tbz`, or `.tbz2` as the file extension.

`-j` Compress (or decompress) an archive using the `bzip2` command.

<img width="613" height="23" alt="Image" src="https://github.com/user-attachments/assets/cadf1b1c-cef4-4ff2-8ef0-6a228c0d6938" />

**2. List Mode**
 I learned that the List mode show the contents of the archive without extracting

Given a `tar` archive, compressed or not, you can see what’s in it by using the `-t` option : `tar -t [-f ARCHIVE] [OPTIONS]`

- `-t` - List the files in an archive.
- `-j` - Decompress with an `bzip2` command.
- `-f ARCHIVE` - Operate on the given archive.

<img width="646" height="154" alt="Image" src="https://github.com/user-attachments/assets/1f77e177-4689-414e-b2d0-50cac6f38d73" />

**2. Extract Mode**
I learned that the Extract Mode pull one or more files out of an archive:

I also learned that you can extract the archive with the `–x` option once it’s copied into a different directory: `tar -x [-f ARCHIVE] [OPTIONS]`

- `-x` - Extract files from an archive.
- `-j` - Decompress with the `bzip2` command.
- `-f ARCHIVE` - Operate on the given archive.

<img width="650" height="267" alt="Image" src="https://github.com/user-attachments/assets/d5997500-a978-442c-9f9d-15dec3e729a1" />

I also learned that adding the `–v` flag, it gives a verbose output of the files processed, making it easier to keep track of what's happening.

`-v` - Verbosely list the files processed.

<img width="646" height="156" alt="Image" src="https://github.com/user-attachments/assets/b022218b-4bcb-44ac-9cd1-392c9110665b" />

 I also learned that If you only want some files out of the archive, add their names to the end of the command, but by default, they must match the name in the archive exactly, or use a pattern.

<img width="615" height="39" alt="Image" src="https://github.com/user-attachments/assets/3fce9920-071d-438e-97de-cdf16427b58b" />

### What I Learned

I learned that `tar` is useful for combining multiple files into a single archive that can later be opened and separated back into its original files.

I also learned that a **tar file**, also called a **tarball** created from multiple files.

Normally, tarball files are slightly larger than the combined input files due to the overhead information on recreating the original files. 

---

### 4. ZIP Files
I learned that in Linux, ZIP is well supported by the `zip` and `unzip` commands. 

The default mode of `zip` is to add files to an archive and compress it: `zip [OPTIONS] [zipfile [file…]]`
- `zipfile` -  The name of the archive to be created, after that, a list of files to be added. 

<img width="645" height="135" alt="Image" src="https://github.com/user-attachments/assets/c5fad79b-08f5-41f4-868a-389eacd4d472" />

The `zip` command will not recurse into subdirectories by default, which is different behavior than the `tar` command. One must use the `–r` option to indicate recursion is to be used.

<img width="644" height="160" alt="Image" src="https://github.com/user-attachments/assets/24802e1d-82fc-4f2b-a3ec-049cee9e9c40" />




I also learned about ZIP files.

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

### What I Learned

I learned another method of creating compressed archives and how to inspect and extract their contents.
