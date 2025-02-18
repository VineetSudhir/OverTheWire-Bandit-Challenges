# Bandit Level 13: Extracting a Password from a Hexdump of a Repeatedly Compressed File

**Objective**
Reconstruct the original file from a hexdump of a repeatedly compressed file to retrieve the next level's password. Use `mktemp -d` to create a secure temporary directory for workspace isolation.

---

**Commands/ Tools Used:**
- mktemp, cp, mv, file, xxd, gzip, bzip2, tar

---

**Solution Steps**

1. Create a Temporary Directory to work on `mktemp -d`.
2. Copy the Original File to the Temporary Directory `cp /home/bandit12/data.txt /tmp/tmp.ehgG9XiZ7U`.
3. Rename the Copied File for clarity, `mv data.txt copy-data.txt`.
4. Create a New Temporary File and move it to the Temporary Directory `/tmp/tmp.ehgG9XiZ7U`, and rename the file:
   `mktemp`
   `mv /tmp/tmp.2KHYFvQupK /tmp/tmp.ehgG9XiZ7U`
   `mv tmp.2KHYFvQupK samplefile1`
5. Convert the Hexdump back to a Compressed Binary File and save the output in, `samplefile1`:
   `xxd -r copy1-data.txt samplefile1`
6. Determine the File Type: `file samplefile1`.
7. Rename the File with the Correct File Extension, `mv samplefile1 samplefile1.gz` to Successfully Decompress the File. Rename the File based on the Output from `file samplefile1`.
8. Decompress the file: `gzip -d samplefile1.gz`.
9. The file is now in **bzip2 format**. Rename and Decompress the Bzip2 File: `bzip2 -d samplefile.bz2`.
10. The file is now in **gzip format again**. Rename and Decompress the Gzip File again: `gzip -d samplefile1.gz`.
11. The file is now in **tar format**. Extract the tar archive `tar --extract --file samplefile1`. This extracts another tar file, `data5.bin`.
12. Extract the Tar Archive Again, `tar --extract --file data5.bin`. This extracts a **bzip2 compressed file**, `data6.bin`.
13. Decompress the Bzip2 File again: `bzip2 -d data6.bin` resulting in a tar file, `data6.bin.out`.
14. Extract the Tar File: `tar --extract --file data6.bin.out`. This extracts a **gzip compressed file**, `data8.bin`.
15. Rename and Decompress the Gzip File:
    `mv data8.bin data8.gz`
    `gzip -d data8.gz`
16. The Final Extracted File, `data8`, contains the **readable text with the password** for the next level.
---

**Tips Learned**
1. Rename files with the correct extension (`.gz, .bz2, .tar`) using `mv` for a successful decommpression.
2. Use a Temporary Directory and Files to prevent accidental data loss and unnecessary files from accumulating in the main working directory.  
