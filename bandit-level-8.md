# Bandit Level 8: Searching for the password next to the word *millionth* in the file data.txt

**Objective:**
Read through the file data.txt for the password to the word 'millionth'. 

---

**Commands/ Tools Used:**
- ls, man, grep

---

**Solution Steps:**

1. Use the `ls -la` command to view all the contents in the 'bandit7' directory in a long-listing format.
   
2. Use the `grep -w "millionth" data.txt` command to view **only** the lines with 'millionth' as a whole word.
   
  
**Tips Learned:**
1. Word Constituent Characters -> letters, digits, & underscore
2. Non-Word Constituent Characters -> all the other characters
