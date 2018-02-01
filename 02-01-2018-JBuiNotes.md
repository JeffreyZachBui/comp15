/**********
02/01/2018
Class notes
**********/

**Pointers**

```
NodeType *curr = head // Curr is now pointed to what head was point
while (curr->next != NULL)
{
    curr = curr->next;
}
delete curr;
```