### Lecture 2 (CS50: Introduction to Computer Science)

**Using C-compiler explicitly**
```
clang -o runme filename.c
./runme

-lcs50 // (if cannot run imported library functions)
```
**Compiling Steps** include:
1. Preprocessing (get to know the imported libraries)
2. Compiling (using assembly code)
3. Assembling (using assembly code into binary code)
4. Linking (linking imported libraries, source code into a executable runnable exe file)

**Debugging Techniques**
- use ``prinf`` for debugging
- use debuggers

A **null** characters mark the end of a *string (array of character)*.

**Command Line Arguments**: Using input when running the program
```
#include <cs50.h>
#include <stdio.h>

// argc : argument count
// argv: argument vector

int main(int argc, string argv[]) // not sure the lenght of your string input

{
  if (argc==2)
  {
    printf("hello, %s\n", argv[1]); // not 0, not 2
  }
  else
  {
    printf("hello, world. \n")
  }

  // aboard the main program execution if something went wrong
  if (argc != 2)
  {
    printf("Missing command-line arguments.\n")
    // to exit the program
    return 1;

    // default is return 0;
  }
}
```

**Terminal**
```
make argv
./argv Name
```

**Cryptography** (using encryption and decryption)
- Plaintext + Key -> Cipher -> Ciphertext
