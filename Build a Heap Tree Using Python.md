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
from binarytree import Node
def _build_bst_from_sorted_values(sorted_values):
    
    if len(sorted_values) == 0:
        return None
    mid_index = len(sorted_values) // 2
    root = Node(sorted_values[mid_index])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right = _build_bst_from_sorted_values(sorted_values[mid_index + 1 :])  
    return (root)

def del_BST(val):
  global x
  if val in x:
    x.remove(val)
    tree=_build_bst_from_sorted_values(sorted(x))
  else:
    return False
  return tree

def display(T):
  for i in T.values:
    print(i,"-->",end="")

x=[3,1,4,2]
print("BST before deletion: ")
t=_build_bst_from_sorted_values(sorted(x))
display(t)
s=int(input())
print("\nBST after deletion: ")
t1=del_BST(s)
display(t1)


```

## OUTPUT
```
![image](https://github.com/user-attachments/assets/0f08944a-050f-4357-8986-ddfe03806b2a)

```

## RESULT
Successfully wrote a Python program to build a heap tree using appropriate Python package and function.
