### Lecture 5 (CS50: Introduction to Computer Science)

- **Memory Reallocation to increase the size of the array dynamically** using ``realloc``
- using the operator of *.* and * as a meaning of moving forward *->* in the context of *struct* data structure

**Linked List**: linking the old information into another information at another memory location
```
typedef struct node
{
  int number;
  struct node *next;
} node;

// Main code
node *list = NULL;
node *n = malloc(sizeof(node));
if (n == NULL)
{
  return 1;
}
n->number = 1;
n->next = NULL;

list = n;

n = malloc(sizeof(node));
if (n == NULL)
{
  free(list);
  return 1;
}

n->number = 2;
n->next = NULL;
list->next = n;

n = malloc(sizeof(node));
if (n == NULL)
{
  free(list->next);
  free(list);
  return 1;
}
n->number = 3;
n->next->next = n;

```
**Memory** is contagious for array.

**NULL's** address is **0x0**.


**Binary Tree Search** running time complexity is *O(log(n))*. Trade off is that you need more pointers to be stored, but you only need to remember your most parent node.

**Hash Table** is a data structure that allows you to associate two different things. It has buckets to put a value. It is a linked list that stored the pointer and direct to many different linked list. It is optimized for fast operations.

**Tries** is where each node is a stored of 26 numbers. Optimized for code reuse efficiency.
