/**********
02/01/2018
Class notes
**********/

**Pointers**




```
Struct NodeType
{
    .char info
    NodeType *next;
}
```

Now every element of this linkedlist is a node type

in the Node Type class

```
NodeType *head
```

Pointers for a linked list

```
NodeType *curr = head // Curr is now pointed to what head was pointing to (head was a pointer to a node type)
while (curr->next != NULL) // next is a member of a structure
{
    curr = curr->next;
}
delete curr;
```

- After deletion of curr, the the last element is gone. 
- curr is still a pointer, but it's just not pointing to the last element on the list cuz nothing is there
- The null gives the indication that theres nothing left in the list.

**LinkedList implementation**

```
Class LL
{
    public:

    private:

        NodeType *head;
        int length
}
```

### Insert function

- Client is going to provide Planet object
- We allocate NodeType on to the **HEAP** as linkedlists grow and shrink on demand
- Set NodeType's info to planet
- Update pointers

initial 

head -> mars/next -> Earth/next -> mercury/next -> Null

Insert Jupitor:

- node |        |
       |--------|
       |        |

- Set node to Jupiter 

       |Jupiter |
       |--------|
       |        |