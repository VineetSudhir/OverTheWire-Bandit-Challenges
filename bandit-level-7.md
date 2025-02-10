# Bandit Level 7: Searching for a File with the Password somewhere in the Server

**Objective:**
Locate and read the file *somewhere in the server* for the password to the next level that has the following properties, 33 bytes, owned by user bandit7, & owned by group bandit6. 

---

**Commands/ Tools Used:**
- ls, cd, find, cat

---

**Solution Steps:**

1. Change to the Home Directory:
- Use the `cd` command to switch from 'bandit6' directory to the 'home' directory
``` cd .. ```

2. Change to the Root Directory:
- Use the `cd` command to switch from the home directory to the root directory
``` cd .. ```

3. Search for Files that have the 3 properties listed above
- Use the ``` find -user bandit7 -group bandit6 -size 33c ``` command
    
4. Read the contents of the file, '.var/lib/dpkg/info/bandit7.password' in the root directory:
- Use the `cat` command to display the password stored in the file:
```
  cat .var/lib/dpkg/info/bandit7.password
```
---

**Tips Learned:**
1. `/` is the Root Directory, the Highest-Level Directory in the System.
   
