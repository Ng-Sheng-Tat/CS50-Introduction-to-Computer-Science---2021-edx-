### Lecture 1 (CS50: Introduction to Computer Science)

**Criteria**
1. Correctness
2. Design good code (clean code)
3. Style

- Compilation converts the source code into binary code that can be run and understands by computers (Machine code) through the use of **compilers**.

**C Code (hello.c)**
```
#include <cs50.h>
#include <studio.h>

int main(void) {

  printf("hello, world\n");

  string answer = get_string("What is your name? ");

  printf("hello, %s\n", answer); // print string here (string place holder)
}
```

**Terminal Command (linux)**
```
make hello
./hello
```
**Linux Command Line**
1. ``rm``: remove
2. ``ls``: list
3. ``mkdir``: make directory
4. ``mv``: move
5. ``rmdir``: remove directory
6. ``cp``: copy
7. ``code``: create a code file

**Data Types**
1. bool
2. char
3. double
4. float
5. int
6. long
7. string

**Place holders**
1. ``%c``
2. ``%f``
3. ``%i``
4. ``%li`` (long integer)
5. ``%s``

**floating-point imprecision**

**Integer Overflow** when you force to put int into float, program discarded the back value after the decimal points

**Data Type Conversion**
```
float (variablename)
```
