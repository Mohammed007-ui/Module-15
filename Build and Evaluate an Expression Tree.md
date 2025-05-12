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
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def is_operator(c):
    return c in ['+', '-', '*', '/']

def evaluate(root):
    if root is None:
        return 0

    # If it's a leaf node (operand), return its value
    if not is_operator(root.value):
        return float(root.value)

    # Evaluate left and right subtrees
    left_val = evaluate(root.left)
    right_val = evaluate(root.right)

    # Apply the operator
    if root.value == '+':
        return left_val + right_val
    elif root.value == '-':
        return left_val - right_val
    elif root.value == '*':
        return left_val * right_val
    elif root.value == '/':
        return left_val / right_val

# Build the expression tree for: (3 + ((5 + 9) * 2))
root = Node('+')
root.left = Node('3')
root.right = Node('*')
root.right.left = Node('+')
root.right.left.left = Node('5')
root.right.left.right = Node('9')
root.right.right = Node('2')

# Evaluate the tree
result = evaluate(root)
print("Result of the Expression Tree:", result)

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/aa0c8320-15b1-425f-975c-b0d654136d0d)


## RESULT:
Successfully wrote a Python program to build and evaluate the given Expression tree.

