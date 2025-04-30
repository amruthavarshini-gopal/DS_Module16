# Ex18 B-Tree

## DATE: 19.03.2025

## Aim:

To write a C function to delete an element in a B Tree.

## Algorithm:

1.Start the program.

2.Try to delete the item from the node using delValFromNode. If not found, print "Not present" and return.

3.If the node's count is 0 after deletion, set tmp to the current node and update myNode to its first linker child.

4.Free the tmp node.

5.Update the global root to the new myNode.

6.Return after deletion.

7.End the program.

## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013 
*/
struct BTreeNode { 
int item[MAX + 1], count; 
struct BTreeNode *linker[MAX + 1]; 
}; 
struct BTreeNode *root;*/ 
void delete (int item, struct BTreeNode *myNode) { 
struct BTreeNode *tmp; 
if (!delValFromNode(item, myNode)) { 
printf("Not present\n"); 
return; 
} else { 
if (myNode->count == 0) { 
tmp = myNode; 
myNode = myNode->linker[0]; 
free(tmp); 
} 
} 
root = myNode; 
return; 
} 
```

## Output:

![438755266-f828337d-3a9e-460c-9894-ecc6bb5c64ce](https://github.com/user-attachments/assets/cdb81fa9-bac7-421b-a7ea-4949b63db33e)

## Result:

Thus, the C function to delete an element in a B Tree is implemented successfully.
