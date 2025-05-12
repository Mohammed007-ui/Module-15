# Ex. No: 15A - Build a Binary Tree with Float Values

## AIM:
To write a Python program to build a binary tree with a root, left, and right node using floating-point values.

---

## ALGORITHM:

1. **Start the program.**
2. **Import** the `Node` class from the `binarytree` module.
3. **Create a root node** using the `Node` class and assign a floating-point value.
4. **Create left and right child nodes** for the root with float values.
5. **Convert the tree** to a list and print the list of nodes.
6. **End the program.**

---

## PYTHON PROGRAM

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

def insert_BST(val):
  global x
  if val in x:
    return False
  else:
    x.append(val)
  tree=_build_bst_from_sorted_values(sorted(x))
  return tree

def display(T):
  for i in T.values:
    print(i,"-->",end="")

x=[5,3,2,4,8,6,10]
print("BST before insertion: ")
t=_build_bst_from_sorted_values(sorted(x))
display(t)
s=int(input())
print("\nBST after insertion: ")
t1=insert_BST(s)
display(t1)


```

## OUTPUT

![image](https://github.com/user-attachments/assets/85b261a3-6114-4533-8635-a155e5081c08)


## RESULT
Successfully  wrote a Python program to build a binary tree with a root, left, and right node using floating-point values.
