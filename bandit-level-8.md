# Bandit Level 8: Searching for the password next to the word *millionth* in the file data.txt

**Objective:**
Read through the file data.txt for the password to the word 'millionth'. 

---

**Commands/ Tools Used:**
- ls, man, grep

---

**Solution Steps:**

1. Use the `ls -la` command to view all the contents in the 'bandit7' directory
   
2. Use the `grep -w "millionth" data.txt` command to view the text on the line that matches with the word 'millionth'.
   - Use the `-w` option to match only the line with whole words, "millionth".
  
**Tips Learned:**
1. Word Constituent Characters -> letters, digits, & underscore
2. Non-Word Constituent Characters -> all the other characters
