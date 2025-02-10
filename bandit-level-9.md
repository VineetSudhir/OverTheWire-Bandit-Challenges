# Bandit Level 9: Searching for the Line that occurs Only Once in a Text File

**Objective**
Search for the password, the line that occurs only once in the text file, *data.txt*, consisting 1001 lines of text.

---

**Commands/ Tools Used:**
- ls, cat, sort, uniq, Piping (|)

---

**Solution Steps:**

1. Use `sort data.txt | uniq -u` command to view the line that occurs only once in the text file, *data.txt*.
   - So that the duplicates are next to each other which can then be detected by `uniq` command.


**Tips Learned**
1. `uniq` command just compares each line to the one directly before it. If duplicates are not next to each other, `uniq` won't recognize them as duplicates.
2. Piping, `|`, is used to connect multiple commands together.
