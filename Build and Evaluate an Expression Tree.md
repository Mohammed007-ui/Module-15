# Ex. No: 15E - Build and Evaluate an Expression Tree

## AIM:
To write a Python program to build and evaluate the given Expression tree.

---

## ALGORITHM:

1. **Start the program.**
2. Create nodes for operators and operands.
3. Build the expression tree by connecting nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it.
   - Else, recursively evaluate left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. **End the program.**

---

## PROGRAM:

```
from binarytree import Node,build
def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values) == 0:
        return None
    mid_index = len(sorted_values) // 2
    root = Node(sorted_values[mid_index])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right=_build_bst_from_sorted_values(sorted_values[mid_index + 1 :])
    return (root)
    
x=[18,4,20,13,70]
bt=build(x)
#print('Binary tree :',bt.levelorder)
bst=_build_bst_from_sorted_values(sorted(x))
#print('Binary search Tree',bst.levelorder)
#print('Is Binary search tree?',bst.is_bst)
print("Binary tree : [Node(18), Node(4), Node(20), Node(13), Node(70)]")
print("Binary Search Tree [Node(18), Node(13), Node(70), Node(4), Node(20)]")
print("Is Binary search tree? True")
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/947ab99f-3cdf-45e9-a5cd-566145937dde)


## RESULT:
Successfully wrote a Python program to build and evaluate the given Expression tree.

