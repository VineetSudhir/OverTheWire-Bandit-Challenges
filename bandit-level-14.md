# Bandit Level 14 - Accessing the Next Level Using an SSH Private Key

**Objective** 
Use the provided private SSH key to authenticate as user `bandit14` on `localhost`, granting access to read `/etc/bandit_pass/bandit14`, which is only readable by user `bandit14`.

---

**Commands/ Tools Used:**
ssh

---

**Solution Steps:**

1. Use `ssh -i /home/bandit13/sshkey.private bandit14@bandit.labs.overthewire.org -p 2220` to log into the next level.
2. Use `cd ..` twice to go to the root directory.
3. Change to the `/etc/bandit_pass` directory and read the 'bandit14' file for the password to the next level.

---

**Tips Learned**
1. Public-Key Cryptography (Asymmetric Encryption) – Uses key pairs (public & private keys) for authentication and encryption. The public key can be shared, but the private key must remain secret for security.
2. Metadata – Public-key encryption secures message content, it does not hide metadata such as sender, time, or message length. Digital Signatures contain metadata to verify authenticity and integrity.
3. `localhost` is a hostname that refers to the same machine, the one I am working on in this case.
