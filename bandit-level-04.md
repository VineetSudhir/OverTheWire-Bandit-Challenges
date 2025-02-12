# Bandit Level 04: Reading the Hidden File for the Password

**Objective:**
Locate and read the hidden file in the 'inhere' directory to retrieve the password for the next level.

---

**Commands/ Tools Used:**
- pwd, ls, cd, cat

---

**Solution Steps:**

1. List contents in the Home Directory:
- Use the `ls` command to display the contents in the directory


2. Change to the 'inhere' Directory:
- Use the `cd` command to switch from the 'home' directory to the 'inhere' directory

3. List All Files in the Directory, including Hidden files:
- Use the `ls -a` command list all the files, including hidden files in the 'inhere' directory
- The `-a` option ensures that hidden files are displayed along with the regular files
  
4. Read the contents of Hidden File named "...Hiding-From-You":
  - Use the `cat` command to display the contents of the hidden file and copy the password:
    
```
  cat ...Hiding-From-You
```
  ---

  **Tips Learned:**
  - Hidden Files start with a dot `.` and `ls-a` doesn't ignore files that start with `.`
  - Quotations or exact file path was not needed here because the filename stats with 3 dots `...`
  - 1 dot `.` and 2 dots `..` have special meanings, anything beyond 2 dots are treated as part of the filename because they have no special meanings to the shell. 
    - 1 dot `.` -> refers to current directory
    - 2 dots `..` -> refers to parent directory
