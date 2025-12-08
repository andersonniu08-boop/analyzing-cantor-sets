# Cantor Set Toolkit

A computational and visualization toolkit for exploring the Cantor set, its finite-stage constructions, and the Cantor function.  

---

## Features

This toolkit provides:

- Construction of the n-th stage Cantor set approximation as a union of intervals  
- Ternary-based membership tests for points  
- Approximation and plotting of the Cantor function  
- Visualization tools for:
  - the interval removal process  
  - stacked iteration stages  
  - the Cantor function graph  

---

## definitions

### The Cantor Set

The middle–third Cantor set is created by iteratively removing open middle thirds.

This begins with:

$$
C_0 = [0, 1].
$$

Remove the middle third:

$$
(1/3, \; 2/3),
$$

leaving:

$$
C_1 = [0, 1/3] \cup [2/3, 1].
$$

Repeating this gives:

$$
C_{n+1} = \frac{1}{3}C_n \;\cup\; 
\left( \frac{2}{3} + \frac{1}{3}C_n \right).
$$

The Cantor set is the limit:

$$
C = \bigcap_{n = 0}^{\infty} C_n.
$$

Thus, we can obser the following characteristics of a cantor set:

- uncountable  
- perfect  
- nowhere dense  

---

## Installation (local dev)

```bash
git clone https://github.com/<andersonniu08-boop>/cantor-toolkit.git
cd cantor-toolkit
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -e .
