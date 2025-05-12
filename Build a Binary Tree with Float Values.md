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
class Node:
    def __init__(self, value):
        self.value = float(value)
        self.left = None
        self.right = None

    def to_list(self):
        result = [self.value]
        if self.left:
            result.extend(self.left.to_list())
        if self.right:
            result.extend(self.right.to_list())
        return result

# Main program
if __name__ == "__main__":
    # Step 3: Create root node
    root = Node(10.5)

    # Step 4: Create left and right child nodes
    root.left = Node(5.2)
    root.right = Node(15.8)

    # Step 5: Convert tree to list and print
    print("Binary Tree as List (Pre-order Traversal):")
    print(root.to_list())

```

## OUTPUT

![image](https://github.com/user-attachments/assets/b57b9f9f-a87d-447c-9879-e71772973ccc)


## RESULT
Thus, the binary tree with floating-point values was successfully created and displayed using a custom implementation.
