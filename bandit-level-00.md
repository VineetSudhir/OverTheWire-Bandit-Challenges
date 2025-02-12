# Bandit Level 00: Connect via SSH

**Objective:**
Learn how to connect to the bandit server using SSH.

---

**Commands/ Tools Used:**
- ssh

---

**Solution Steps:**
1. Connect to the Bandit server using SSH
 ```
ssh bandit0@bandit.labs.overthewire.org -p 2220 
```
2. Explanation
- For this level the **host**, **port**, **username**, and **password** are provided.
- The **@** symbol is used to combine the username (bandit0) with the host (bandit.labs.overthewire.org) in the SSH command to log in successfully. 
- The **-p 2220** specifies the port, as the Bandit server uses port 2220 instead of the default SSH port 22.

3. Close the Bash session:
```
exit
```
- This command logs you out of the Bandit server and returns you to your local terminal
