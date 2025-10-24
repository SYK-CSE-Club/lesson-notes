# Session Summary: Intro to Competitive Programming, Datatähti, IOI, CSES & Algorithms

## What We Covered

- **What is Competitive Programming (CP)?**
	- Why do it? What skills does it build?

- **CSES Platform (cses.fi):**
	- What is [CSES](https://cses.fi/)? How to use it?
    - For practicing problems
	- Creating accounts and exploring the problemset
	- [CSES Problem Set](https://cses.fi/problemset/)

- **What is IOI?**
	- The International Olympiad in Informatics
	- How Datatähti is the Finnish national informatics competition and is the road to IOI

- **Datatähti:**
	- How to join
  - The [datatahti.fi](https://datatahti.fi) website
	- How the competition works, registration, and structure
    - Prelim round happens online: lasts 2 weeks. Then those who qualify attend the finals.

- **Time Complexity & Big O Notation:**
	- What is time complexity? Why does it matter?
	- Big O notation
  - Operations per second for most computers
  - The typical time limit of 1 second in CP

- **CSES Problems Solved in Class:**
	- [General CSES problem set: Weird Algorithm](https://cses.fi/problemset/task/1068/)
	- [Datatähti problem set: Pisin toisto (Longest Repetition)](https://cses.fi/dt/task/317)

Note: Weird Algorithm is not an actual algorithm, its just a name for the problem.

- **Important Concepts Discussed:**
	- Taking input from the system
	- What is an edge case and how to handle them

- **The Competitive Programmer's Handbook:**
	- What it is, where to find it, and how to use it
	- [Book PDF](https://cses.fi/book/book.pdf)

- **Stairs Problem:**
	- If you can take 1 or 2 step jumps going up a staircase, how many ways to reach the nth step?
	- Recognizing the pattern (it's a Fibonacci sequence)
	  - Recursion
      - What is it
      - How to implement it in code
      - Is what Dynamic programming (DP) is based on --> definig a term using the terms before it
	- Whiteboard/drawing explanation


## Python Solutions

**Weird Algorithm:**
```python
n = int(input())
while n != 1:
	print(n, end=' ')
	if n % 2 == 0:
		n //= 2 # or: n = n // 2
	else:
		n = n * 3 + 1
print(1)
```

**Pisin toisto (Longest Repetition):**
```python
dna = input()

counter = 1
best = 1

for i in range(1, len(dna)): # 1, 2, 3, 4, ... , n - 1
    if dna[i] == dna[i - 1]:
        counter += 1
        best = max(best, counter)
    else: 
        counter = 1

print(best)
```

**Ways to Climb Stairs:**
```python
def ways(n):
	if n == 0 or n == 1:
		return 1
	return ways(n-1) + ways(n-2)

n = int(input())
print(ways(n))
```

## Relavent Documents:

### The Competitive Programmer's Handbook:

- Access online: [Book PDF](https://cses.fi/book/book.pdf)
- Or in this GitHub repo: [Book PDF](book.pdf)

## Homework: 

**Optional:**

- Participate in the datatähti and/or do exercises in CSES if you wish
- Try to solve at least 2 new problems from the CSES/Datatähti Problem Set in CSES (choose any topic you like)
- Read the first two chapters of the Competitive Programmer's Handbook