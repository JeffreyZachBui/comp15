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

    - Update pointers so we can insert jupiter to the front of the LinkedList

- Head WAS pointing to the front of the list, so we want head to be pointing to Jupiter
- node->next = head
  head = node

```
void LinkedList::insert_planet(Planet p)
{
    NodeType *node = new NodeType; // allocated NodeType on heap
    node->info = p; // Setting the NodeType's info to planet, 
    node->next = head
    head = node;
    length++
}
```

because it is a pointer to an object, we use arrows.
 ```   
(*node).info = p = node->info
```

How make a find function

- Create while loop for as long as node isn't pointing to the NULL
- node->info == p
- returmn node -> info


**Copy Constructors + Rule of 3**

If your class has dynamic memory then u must write:

1) A destructor -> Deallocate memory once object goes out of scope
2) Copy constructor
3) Assignment opertator

```

Class LinkedList
{
    public:


    private:

        NodeType *head;
}

```

```
LinkedList l;
LinkedList l2;
// more code
l = l2; // what this does is that l and l2 are pointing to the EXACT same spaces in memory so if you do l2.insert(pluto) both l and l2 will have pluto
```
The assignment operater = results in SHALLOW COPYING. Thus, we need copy constructor

**Copy Constructor** is for deep copying and is when we **pass by value**

so now 

```
l2.insert(pluto)
foo(l); //invokes copy constructor
```