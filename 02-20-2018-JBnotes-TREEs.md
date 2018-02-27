/**********
02/20/2018
Class notes
**********/


Outline:
1. BST run-time complexity
2. Self-balancing trees
3. Project Questions



**BST run-time complexity**
- insert
- delete
- find
- traversal
- print
- make empty
- length
- copy constructor/assignment
- number of leaves
- get height

**Difference** between length and height for trees 
- To get lenght of a tree -> number of nodes
    -> count number of left subtree
    -> count number of right subtree
    -> Then add 1
    -> If subtree is linkedlist (degenerated tree), then heigh = length
- Height of other tree is how low the roots are
Thus:
    - length = number of nodes
    - height = how low it goes
    - O(n) lln is the number of nodes 

**Destructor(BT/BST)**
- destroy left subtree
- destroy right subtree
- delete myself
- O(n)

**find (BST)**
- base case(empty tree)
- If found, return
- search in left subtree **OR** in right subtree 
- linear in the hieght of the tree 
    O(h)

**2.Self Balancing BSTs**
- Full binary tree:
    - envery non leagf node has 2 children
- halanced tree

**Self blancing trees**
- AVL trees
-Red black trees

**3. Project Questions**

typedef:
void BT:: insert(Treeitem)

typedef [actual thing] [new name]

typedef int laney
laney x = 5;

**BST/BT** copy constructor
- tree to copy (param)
- tree who wants to be a copy

INt the function:
= Allocate new Binary Node
- Update node's value from the source
- do the same with subtrees

root = new BinaryNode
root->info = source.root.value
// make copy of left sub tree
// make copy of right sub tree
(destination)
'