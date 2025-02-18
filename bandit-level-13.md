# Bandit Level 13: Extracting a Password from a Hexdump of a Repeatedly Compressed File

**Objective**
Reconstruct the original file from a hexdump of a repeatedly compressed file to retrieve the next level's password. Use `mktemp -d` to create a secure temporary directory for workspace isolation.

---

**Commands/ Tools Used:**
- mktemp, cp, mv, file, xxd, gzip, bzip2, tar

---

**Solution Steps**

1. Create a temporary directory to work on `mktemp -d`.
2. Copy the original file, `/home/bandit12/data.txt` to the newly created temp directory, `/tmp/tmp.ehgG9XiZ7U`.
3. Rename the copied file in the temp directory to prevent any confusion, `mv data.txt copy-data.txt`.
4. Create a temp file, move it to the temp directory, `/tmp/tmp.ehgG9XiZ7U`, and rename it, 'samplefile1' to write the output from reverting the hexdump file `data.txt` to the file.
   `mktemp`
   `mv /tmp/tmp.2KHYFvQupK /tmp/tmp.ehgG9XiZ7U`
   `mv tmp.2KHYFvQupK samplefile1`
5. Revert the hexdump file to the compressed format, `xxd -r copy1-data.txt samplefile1` and save the output to the 'samplefile1` file.
6. Use `file samplefile1` to find out what type of compressed format it is in.
7. Rename the file with the appropriate file extension, `mv samplefile1 samplefile1.gz` to successfully decompress the file.
8. Decompress the file, `gzip -d samplefile1.gz`
9. The file is now in bzip2 compressed format, so rename file with the extension `bz2` to decompress the file,
    `bzip2 -d samplefile.bz2`
10. The file is now in gzip compressed format again. Rename and decompress again, `gzip -d samplefile1.gz`.
11. The file is now in a tar file format. extract the archive with `tar --extract --file samplefile1` to get another tar formatted file `data5.bin`.
12. Extract again, `tar --extract --file data5.bin` to get a bzip2 compressed formatted file, `data6.bin`.
13. Decompress again, `bzip2 -d data6.bin` to get a tar file format, `data6.bin.out`.
14. Extract again, `tar --extract --file data6.bin.out` to get a gzip compressed formatted file, `data8.bin`.
15. Rename the file with the correct file extension `.gz` and decompress again, `gzip -d data8.gz` to get the original file with readable text containing the password to the next level `data8`.

---

**Tips Learned**
1. Add the appropriate file extension to the filename by renaming using `mv` for the commands, `gzip` & `bzip2`.
2. Use a temporary directory and files to prevent data loss and prevents unnecessary files from accumulating in the main working directory.  
