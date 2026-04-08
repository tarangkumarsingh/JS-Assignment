# JS-Assignment

## Assignment 4 - Fundamentals of Web Design

**Author:** Tarang Kumar Singh

---

### Q1 - Digit Gatekeeper

**Approach:** Iterate through every integer from L to R. For each integer, check divisibility by K, verify no digit is 0 by scanning each character, compute the digit sum, and test primality using trial division up to the square root.

**Complexity:** O((R - L) * D) where D is the max number of digits in any number in the range.

---

### Q2 - Roll-Seed Lock

**Approach:** Start with N and apply the transformation rule 3 times in a loop: divide by 2 and add seed if even, otherwise multiply by 3 and subtract seed. After 3 iterations, convert the result to a string and check whether it falls in the 100-999 range and the middle (second) digit equals seed.

**Complexity:** O(1) since exactly 3 iterations are performed.

---

### Q3 - Mirror Corridor

**Approach:** Iterate X from 0 to 100000. For each candidate, check if N+X is a palindrome by comparing characters from both ends of its string representation, and check divisibility by K. Return the first valid X found, or -1 if none exists.

**Complexity:** O(100000 * D) where D is the number of digits, effectively O(1) since the upper bound is fixed.

---

### Q4 - Fare Calculator

**Approach:** Compute the fare step by step following the given rules: base + 7*distance, add late penalty if applicable, add 10% surcharge (floored) if distance exceeds 10, adjust by seed based on parity, and finally round up to the nearest multiple of 5 using modular arithmetic.

**Complexity:** O(1) since all operations are constant time.

---

### Q5 - Skipping Numbers

**Approach:** Increment m starting from 1. For each m, if m is not divisible by (seed+2), add it to a running sum. Stop when the sum reaches or exceeds N. Report both m and the final sum.

**Complexity:** O(m) where m is the answer value, bounded by the constraint on N.

---

### Q6 - Contest Score Judge

**Approach:** Compute score = 3a + b - 2c. Clamp negative scores to 0. Apply a 10-point penalty if total submissions exceed 50. Determine PASS (score >= 60) or FAIL status.

**Complexity:** O(1) since all operations are constant time.
