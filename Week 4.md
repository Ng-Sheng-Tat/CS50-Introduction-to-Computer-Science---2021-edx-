### Lecture 4 (CS50: Introduction to Computer Science)

**RGB**: represents as
1. R:xx
2. G:xx
3. B:xx

**Hexadecimal**
- *01234567ABCDEF*
- "0A" represents "8"
- base-16
- maximum can count to 255, including 0, so there will be 256 characters
- 0xB = B (in hexadecimal denotation)
- 0x10 = 16

**Memory Address**
- variables are stored in memory
- *variables information* store the values in memory address
```
int n = 50;
int *address = &n;
// print the address
printf("%p\n", address);
// print the values stored in the address
printf("%p\n", p)
printf("%i\n", *p) // dereferencing
```
- pointers variable normally put out 8 bytes
- string variable name actually is a pointer to the first character of the string values, hence the argument can be made
```
string s = "string text";
// is equivalent to
char *s = "string text";
printf("%p\n", s);
// is equivalent to
printf("%p\n", &s[0]);
```

**Pointer Arithmetic**
```
char *s = "text";
printf("c\n", *s);
printf("c\n", *(s+1));

int numbers[] = {0,1,2,3,4,5,6};
printf("%i\n", *numbers);
printf("%i\n", *(numbers+1));
```

**They refer to the same memory address**
```
string s = get_string("s: ");
string t = s;
t[0] = toupper(t[0]);
// both t and s are now capitalized
```

**Dynamics Memory Allocation**
1. ``malloc``: means memory allocation (returning an address)
2. ``free``: means free up the memory
- they come in pair
- a well-designed program should consume memory and free-up memory so that it will runs fast without clashing

```
#include <ctype.h>
#include <stdlib.h>
char *s = get_string("s: ");
// put the number of bytes inside the momory space, one is for "\0"
char *t = malloc(strlen(s) + 1);
// Method 1
for (int i = 0; n = strlen(s) + 1; i < n; i++)
{
  t[i] = s[i];
}
// Method 2
strcpy(t, s);
// free up memory
free(t);
// not need to free s due to it will be handled by libraries of c
// to avoid memory leak
```
- *NULL* is 0 in the pointers (to check a pointer is valud or not)

**Tools for debugging memory related problems**
- in command windows
``valgrind ./executablefilename``

**Code Loading Preferences**
1. Machine Code
2. Global Variables
3. Heap/Stack (problems creation from bi-direction heading towards each other, leading to *stack-overflow*)
