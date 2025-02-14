# Bandit Level 12: Decrypting Rot13

**Objective** 
The lowercase (a-z) and uppercase (A-Z) letters of the password have been rotated by 13 positions. Rotate it 13 positions again to retrieve the original password.

---

**Commands/ Tools Used:**
- ls, cat, tr, Piping (|)

---

**Solution Steps**

1. Use the `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'` to rotate the letters by 13 positions again, retreiving the original password.

---

**Tips Learned**
1. `tr 'A-Za-z' 'N-ZA-Mn-za-m'` can be used to shift the all the letters by 13 positions.
2. Similarly, `tr 'A-Za-z' 'M-ZA-Lm-za-l'` can be used to shift all the letters by 12 positions.
   - `'A-Za-z'` ensures all the uppercase and lowercase alphabets shift positions as defined in the second array.
