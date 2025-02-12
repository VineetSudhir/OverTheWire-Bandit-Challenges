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
1. **ASCII** in modern systems are 8-bit byte, no longer 7-bits.
2. When encoding to Base64, the original plain text is first converted to 8-bit binary data and grouped.
3. Then grouped to **24-bit chunks**, as Base64 **always** processes data in 24-bit chunks. If data doesn't fit into 24-bit groups, **padding** is used make it a 24-bit   chunk.
4. The 24-bit chunks are split into **6-bit segments** and mapped to **Base64** characters.
