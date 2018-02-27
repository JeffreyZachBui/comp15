/**********
02/27/2018
Class notes
**********/

**Axuilary Data Structures**

-  Temporanrily used to assist a primary data structure in solving a problem

Stacks
- Goal is to sum all in a Stacks
- Keep stack intact

Simple Destructive Method
- Pop everything off
- Sum as we Goal

Not Destructive
- Make  deep copy -  auxilary stack object
- Do same as above

 LEARN QUEUES

 transferring stack to que

 ```
ItemType Stack::sum()
{
    double sum  =  0;
    Queue q;
    while(!is_empty())
    {
        double x += top();
        sum += x;
        q.enqueue;
        pop();
    }

    Stack s;
    while (!q.is_empty())
    {
        s.push(q.dequeue());
    }

    while (!s.is_empty())
    {
        push(s.top());
        s.pop();
    }
    return sum;
}
```

**Exam**

1. Run time complexity
    - Similar to worksheets
    - Upper bound of a funcion
    - Runtime vs size
    - Data Structures:
        - ArrayList
        - Linkedlists
        - Stacks
        - Queues
        - BTs
        - BSTs
        - AVL (know the advantages)
2. ADT diagrams - if you insert an element, be able  to draw
    - if you insert this what happens?
    - Cover what happens in memory
    - Be able to draw
        - What happens when you make copy of pointer
        ```
        BN *p;
        BN *p2 = p;
        ```
        Both just point to heap
3. Designing + writing code
    - Revisiting  functions
    - Looking at data structures then writing  functions in diff way
    - No need for assignment operator function prototpye but body
    - Recursive helper function
    - Rule of 3
    - Inheritance
    - Virtual
    - Constructors
    - Destructors
    - Inheritance
    - Order:
        - eg constructor for BTs
        - base class first
        - derive class fist
        - consturctor other way
    - Tell whether assignment operator or copy constructor
    