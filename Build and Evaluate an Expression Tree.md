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

def evaluate(root):
    # If leaf node (operand)
    if root.left is None and root.right is None:
        return float(root.value)
    
    # Evaluate left and right subtrees
    left_val = evaluate(root.left)
    right_val = evaluate(root.right)
    
    # Apply operator at root
    if root.value == '+':
        return left_val + right_val
    elif root.value == '-':
        return left_val - right_val
    elif root.value == '*':
        return left_val * right_val
    elif root.value == '/':
        return left_val / right_val

# Build the expression tree for (3 + ((5 + 9) * 2))
root = Node('+')
root.left = Node('3')

right_subtree = Node('*')
right_subtree.left = Node('+')
right_subtree.left.left = Node('5')
right_subtree.left.right = Node('9')
right_subtree.right = Node('2')

root.right = right_subtree

# Evaluate the expression tree
result = evaluate(root)
print("Result of the expression tree evaluation:", result)

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/1be11bf1-de06-47ba-8949-a4e24f5a76ea)


## RESULT:

The program successfully builds and evaluates the expression tree representing the expression 3 + ((5 + 9) * 2) and outputs the correct result.
