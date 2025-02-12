# Bandit Level 02: Reading the `-` File for the Password

**Objective:**
Locate and read the file named '-' in the home directory to retrieve the password for the next level.

---

**Commands/ Tools Used:**
- pwd, ls, cat

---

**Solution Steps:**
1. Verify You're in the Home Directory:
- Use the `pwd` command to confirm you're in the home directory


2. List contents in the Home Directory:
- Use the `ls` command to display the contents in the directory


3. Read the Contents of the '-' File:
- Use the `cat` command to display the contents of the file and copy the password:
  
  ```
  cat /home/bandit1/-
  ```
  ---

  **Tips Learned:**
  - `-` is a special character in Unix/ Linux systems, typically interpreted as an option or standard input by commands like `cat`.
  - Using the exact file path makes the `cat` command treat `-` as a filename rather than an option.
  - Or, use `--` to signal the end of options, treating everything after `--` as a filename.

  ```
  cat -- -
  ```
