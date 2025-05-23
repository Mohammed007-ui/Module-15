# Ex. No: 15D - Build a Heap Tree Using Python

## AIM:
To write a Python program to build a heap tree using appropriate Python package and function.

---

## ALGORITHM:

1. **Start the program.**
2. Import the `heapq` module.
3. Define a function `heaptree(H)` that takes a list `H` as input.
4. Use `heapq.heapify(H)` to convert the list into a min-heap.
5. Print the created heap.
6. **End the program.**

---

## PROGRAM:

```
import heapq

def heaptree(H):
    heapq.heapify(H)  # transforms list H into a min-heap in-place
    print("Heap tree:", H)

# Example list of float values
H = [3.2, 1.5, 4.8, 2.9, 7.1, 0.5]

print("Original list:", H)
heaptree(H)

```

## OUTPUT

![image](https://github.com/user-attachments/assets/4203c58d-7dd6-4062-982c-378f62b3e5a6)


## RESULT
The program successfully builds a min-heap tree from a list of float values using Python's heapq module. The heapify() function rearranges the list so that the smallest element is at the root, satisfying heap properties.

