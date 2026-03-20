# The Alasmine Theorem
### A Deterministic Exploration of the 3n+3 Dynamical System

**Author:** Samar (Class 8 Student)  
**Date:** March 2026  
**Location:** India  

---

## 📌 Overview

This project investigates a modified version of the Collatz function:

f(n) = (3n + 3) / 2^v

where v = v_2(3n+3) is the highest power of 2 dividing (3n+3).

The goal is to explore whether this system exhibits global convergence, and whether all positive integers eventually reach a fixed point.

---

## 🎯 Key Idea

Unlike the classical 3n+1 problem, replacing +1 with +3 introduces structural regularity:

- Every odd step produces a multiple of 3  
- This creates a restricted domain (multiples of 3)  
- The system may behave more predictably due to this constraint  

---

## 🧠 Core Observations

### 1. Capture into Multiples of 3

3n + 3 = 3(n+1)

All values enter the set of multiples of 3 after one odd step.

---

### 2. Modular Classification (mod 4)

All integers are classified as:

- 4k
- 4k+1
- 4k+2
- 4k+3

Behavior:

- Even numbers reduce via division by 2  
- Odd numbers transform via 3n+3

---

### 3. Behavior of 4k+1

n = 4k+1

3n+3 = 12k+6

(12k+6)/2 = 6k+3

- If k is even → enters 4k−1 class  
- If k is odd → remains in 4k+1  

---

### 4. Binary Carry Argument

Binary representation:

- 4k+1 → ends in ...01  
- Adding +3 (=11 in binary) introduces carry propagation  

This suggests:

- At least one division by 2 always occurs  
- Sometimes multiple divisions occur (carry avalanche)

---

### 5. Bit Growth vs Decay (Heuristic)

- Multiplying by 3 increases size (~1.58 bits)  
- Division by 2^v decreases size  

Hypothesis:

Over time, decay dominates growth → sequence shrinks

---

## 🔁 Fixed Point Analysis
t
Solve:

n = (3n+3) / 2^v

n(2^v − 3) = 3

n = 3 / (2^v − 3)

Checking integer solutions:

- v = 2 → n = 3 ✅  
- No other positive integer solutions exist

For Multiple step cycles 3^m must be equal to 2^n
Because of the coprimality it can't exist.

Conclusion:  
The only fixed point is n = 3

---

## ⚠️ Known Gaps / Open Questions

This is an exploratory proof attempt. Some steps are not fully rigorous:

1. It is not formally proven that all sequences eventually leave the 4k+1 class  
2. The binary carry argument is heuristic, not fully formalized  
3. Multi-step cycles (length > 1) are not completely ruled out  
4. Bit decay argument is approximate, not strict  

---

### Note : This is a description of my proof check the pdf file for the full.

## 🤔 Main Question

Is the following claim valid?

All positive integers under this system eventually converge to 3.

If not, where does the reasoning break?

---

## 📊 Future Work

- Analyze behavior under mod 8 or mod 16  
- Study v_2(3n+3) distribution  
- Attempt formal proof of finite escape from 4k+1  
- Investigate possibility of non-trivial cycles  

---

## 🙏 Feedback Welcome

I am a student exploring number theory and dynamical systems.  
Any feedback, corrections, or suggestions are highly appreciated.
Note: I have made this proof with the contribution and partnership with Google AI.
---

## ⭐ Note

This is not claimed as a complete proof, but as a structured attempt toward understanding the system.
