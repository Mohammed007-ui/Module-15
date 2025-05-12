# Ex. No: 15C - Expression Tree with Inorder and Postorder Traversal

## AIM:
To write a Python program to build the given expression tree and print the inorder and postorder traversals.

---

## ALGORITHM:

1. **Start the program.**
2. Import the required modules (`build` and `Node` from `binarytree`).
3. Define a list `x` representing the expression tree in pre-order fashion (with `None` for missing nodes).
4. Use the `build()` function to generate the binary tree.
5. Print the **inorder** and **postorder** traversal of the tree.
6. **End the program.**

---

## PROGRAM:

```
from binarytree import Node

def _build_bst_from_sorted_values(sorted_values):
    
    if len(sorted_values)==0:
        return None
    mid_index = len(sorted_values)//2
    root=Node(sorted_values[mid_index])
    root.left=_build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right=_build_bst_from_sorted_values(sorted_values[mid_index+1:])
    return root

def left_subtree(l):
    print("Left Subtree : ")
    for i in l[1].values:
        print(i,"-->",end="")
    return 


a=[]
size=int(input())
for i in range(0,size):
    val=int(input())
    a.append(val)
x=sorted(a)

l=_build_bst_from_sorted_values(x)
print("Postorder :",l.postorder)
left_subtree(l)
print("\nIs this a Binary Search Tree? ",l.is_bst)

```

## OUTPUT

![image](https://github.com/user-attachments/assets/4e9f4c06-b585-4391-8a82-e22ffa66818b)



## RESULT
Successfully wrote a Python program to build the given expression tree and print the inorder and postorder traversals.
