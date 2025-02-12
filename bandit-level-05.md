# Bandit Level 05: Reading the Only Human-Readable File for the Password

**Objective:**
Locate and read the Only Human-Readable file in the 'inhere' directory to retrieve the password for the next level.

---

**Commands/ Tools Used:**
- ls, cd, file, cat

---

**Solution Steps:**

1. Change to the 'inhere' Directory:
- Use the `cd` command to switch from the 'home' directory to the 'inhere' directory

2. View the file type for all files in the 'inhere' directory:
- Use the `file` command to view the file type for each file
```
file ./*
```
3. Read the contents of the Only Human-Readable file type named "-file07":
  - Use the `cat` command to display the password in the file to copy:
    
```
  cat ./-file07
```
---

**Tips Learned:**
  - Asterisk `*` Wildcard, can be used to reference all files
