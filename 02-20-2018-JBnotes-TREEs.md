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

**Destructor**
- destroy left subtree
- destroy right subtree
- delete myself
- O(n)