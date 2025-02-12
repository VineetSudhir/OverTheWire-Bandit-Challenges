# Bandit Level 11: Decode Base64 Encoded Data to Find the Password in `data.txt`

**Objective**
Locate and decode the Base64-encoded data in data.txt to retrieve the password for the next level.

---

**Commands/ Tools Used:**
- ls, cat, base64

**Solution Steps**

1. Use the command `base64 -d data.txt` to decode the Base64-encoded content in `data.txt` and retrieve the original plain text.

---

**Tips Learned**
1. **Base64**, originally used to encode binary data, can also be used to encode plain text.
