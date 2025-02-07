# Bandit Level 6: Searching for a File with the Password based on its Properties

**Objective:**
Locate and read the file that is 1033 bytes in size, human-readable, & not executable in the 'inhere' directory to retrieve the password for the next level.

---

**Commands/ Tools Used:**
- ls, cd, find, file, cat

---

**Solution Steps:**

1. Change to the 'inhere' Directory:
- Use the `cd` command to switch from the 'home' directory to the 'inhere' directory

2. Find Files that are 1033 Bytes in Size:
- Use the `find` command to list all the files that are 1033 bytes in size
```
find -size 1033c
```
- The `c` specifies the size in bytes. Only one file matches this size.

3. Check if the File is Human-Readable:
- Use the `file` command to verify the file type is human-readable:
```
file ./maybehere07/.file2
```

4. Check if the File is Not Executable:
- Use the `ls -l` command to display files & directories in a Long Listing Format:
```
ls -l ./maybehere07/.file2
```
- Check the file permissions to confirm that the file is not executable
    
5. Read the contents of the file, './maybehere07/.file2' in the 'inhere' directory:
- Use the `cat` command to display the password stored in the file:
```
  cat ./maybehere07/.file2
```
---

**Tips Learned:**
1. Using the `find` Command with Size Options:
   - Use `c` for bytes, `k` for kilobytes, `M` for megabytes, and `G` for gigabytes.

2. Understanding `ls -l` for File Details:
```
-rw-r----- 1 root bandit5 1033 Sep 19 07:08 ./maybehere07/.file2
```
   - `rw-r-----` -> file type and permissions
   - `1` -> number of links
   - `root` -> owner of the file
   - `bandit5` -> group associated with the file
   - `1033` -> file size in Bytes
   - `Sep 19 07:08` -> time & date of the last time the file was modified
   - `./maybehere07/.file2` -> names of the directory and file
     
2a. **First Character** in the **file type and permissions**
   - `-` -> regular file
   - `d` -> directory
   - `l` -> symbolic link

2b. Next **Nine Characters** are grouped into sets of three, representing the permissions for the owner, group, and others:
   - `r` -> read permission
   - `w` -> write permission
   - `x` -> execute permission 
  
   *Link: https://linuxconfig.org/understanding-of-ls-command-with-a-long-listing-format-output-with-permission-bits*
