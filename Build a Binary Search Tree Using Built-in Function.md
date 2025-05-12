# Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

## AIM:
To write a Python program to build a binary search tree using a built-in function.

---

## ALGORITHM:

1. **Start the program.**
2. Define `_build_bst_from_sorted_values(sorted_values)` to recursively build a binary search tree (BST) from a sorted list.
3. Define `left_subtree(l)` to print the left subtree of the BST.
4. Take user input for the number of elements and store the values in a list `a`.
5. Sort the list and pass it to `_build_bst_from_sorted_values()` to construct the BST.
6. Print the postorder traversal of the BST.
7. Call `left_subtree(l)` to print the left subtree.
8. Check whether the tree is a binary search tree using the `is_bst` property.
9. **End the program.**

---

## PROGRAM:

```
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key

# Function to insert a new node with the given key
def insert(root, key):
    if root is None:
        return Node(key)
    if key < root.val:
        root.left = insert(root.left, key)
    else:
        root.right = insert(root.right, key)
    return root

# Function to perform postorder traversal
def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.val, end=' ')

# Function to print left subtree
def left_subtree(root):
    print("Left Subtree: ", end='')
    postorder(root.left)
    print()

# Function to check if a tree is BST
def is_bst_util(node, left, right):
    if node is None:
        return True
    if (left is not None and node.val <= left.val) or (right is not None and node.val >= right.val):
        return False
    return is_bst_util(node.left, left, node) and is_bst_util(node.right, node, right)

def is_bst(root):
    return is_bst_util(root, None, None)

# Main program
if __name__ == "__main__":
    n = int(input("Enter number of elements: "))
    a = []
    for i in range(n):
        a.append(int(input(f"Enter element {i+1}: ")))

    root = None
    for key in a:
        root = insert(root, key)

    print("\nPostorder traversal of BST:")
    postorder(root)

    print()
    left_subtree(root)

    if is_bst(root):
        print("The tree is a Binary Search Tree.")
    else:
        print("The tree is NOT a Binary Search Tree.")

```

## OUTPUT

![image](https://github.com/user-attachments/assets/59d5bc43-fd57-4f29-adf2-59f3f9de1813)


## RESULT
Thus, the Python program to build a Binary Search Tree (BST), print postorder traversal, display the left subtree, and check if it's a BST has been successfully implemented and verified.
