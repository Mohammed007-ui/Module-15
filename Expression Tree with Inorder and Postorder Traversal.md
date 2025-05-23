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
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def inorder(root):
    if root:
        inorder(root.left)
        print(root.value, end=' ')
        inorder(root.right)

def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.value, end=' ')

# Build the expression tree for (3 + ((5 + 9) * 2))
root = Node('+')
root.left = Node('3')

right_subtree = Node('*')
right_subtree.left = Node('+')
right_subtree.left.left = Node('5')
right_subtree.left.right = Node('9')
right_subtree.right = Node('2')

root.right = right_subtree

print("Inorder traversal:")
inorder(root)  # Expected: 3 + 5 + 9 * 2
print("\nPostorder traversal:")
postorder(root)  # Expected: 3 5 9 + 2 * +

```

## OUTPUT

![image](https://github.com/user-attachments/assets/213f2598-7175-43bb-b492-be3d35ce88cf)

## RESULT
The program builds the expression tree and correctly prints its inorder and postorder traversals.
