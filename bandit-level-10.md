# Bandit Level 10: Find the Password Hidden Among the Few Human-Readable Strings 

**Objective**
Search for the password stored in the data.txt file in one of the few human-readable strings, preceded by several '=' characters.

---

**Commands/ Tools Used:**
- ls, cat, strings, grep, Piping (|)

---

**Solution Steps:**

1. Use the `strings -a data.txt | grep "="` command to scan the entire `data.txt` file to filter out only the human-readable strings and display those that contain one or more '=' characters.

---

**Tips Learned**
1. The `a` option in `grep` is used to process binary files as text.
