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
    print("Original List:", H)
    heapq.heapify(H)
    print("Heapified Tree (Min-Heap):", H)

# Main program
H = [25, 14, 9, 30, 18, 7, 4, 12]
heaptree(H)



```

## OUTPUT


![image](https://github.com/user-attachments/assets/43de4774-5da1-49a2-9a21-62f4baaa451c)


## RESULT
Successfully wrote a Python program to build a heap tree using appropriate Python package and function.
