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
# Define the Node class
class Node:
    def __init__(self, data):
        self.data = data       # float value stored in the node
        self.left = None       # left child node
        self.right = None      # right child node

# Create root node with float value
root = Node(10.5)

# Create left and right children with float values
root.left = Node(5.2)
root.right = Node(15.8)

# Function to print the tree in preorder traversal
def preorder(node):
    if node:
        print(node.data, end=" ")
        preorder(node.left)
        preorder(node.right)

# Print the tree nodes in preorder
print("Preorder traversal of the binary tree:")
preorder(root)

```

## OUTPUT
```
![image](https://github.com/user-attachments/assets/72fecc5e-f340-4e5c-8bf4-b1379b258cd9)

```

## RESULT
The program successfully builds a binary tree with float values for the root and its left and right children. The preorder traversal displays the values in the expected order.
