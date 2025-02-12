# Bandit Level 03: Reading the `spaces in this filename` File for the Password

**Objective:**
Locate and read the 'spaces in this filename' file in the home directory to retrieve the password for the next level.

---

**Commands/ Tools Used:**
- pwd, ls, cat

---

**Solution Steps:**
1. Verify You're in the Home Directory:
- Use the `pwd` command to confirm you're in the home directory


2. List contents in the Home Directory:
- Use the `ls` command to display the contents in the directory


3. Read the Contents of the 'readme' File:
- Use the `cat` command to display the contents of the file and copy the password:
  
  ```
  cat "spaces in this filename"
  ```
  ---

  **Tips Learned:**
  - Use quotes `"spaces in this filename"` for `cat` command to treat it as a filename rather than separate arguments.
  - Otherwise, `cat` would treat "spaces", "in", "this", and "filename" as separate arguments.
