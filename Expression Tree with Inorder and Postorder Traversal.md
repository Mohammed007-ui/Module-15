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

# Build the expression tree manually: ((3 + 5) * (6 - 2))
root = Node('*')
root.left = Node('+')
root.right = Node('-')
root.left.left = Node('3')
root.left.right = Node('5')
root.right.left = Node('6')
root.right.right = Node('2')

def inorder(node):
    if node is None:
        return []
    return inorder(node.left) + [node.value] + inorder(node.right)

def postorder(node):
    if node is None:
        return []
    return postorder(node.left) + postorder(node.right) + [node.value]

print("Inorder Traversal: ", ' '.join(inorder(root)))
print("Postorder Traversal: ", ' '.join(postorder(root)))


```

## OUTPUT

![image](https://github.com/user-attachments/assets/c4088e3f-6c54-49eb-8c58-24d387f5af9e)


## RESULT
Successfully wrote a Python program to build the given expression tree and print the inorder and postorder traversals.
