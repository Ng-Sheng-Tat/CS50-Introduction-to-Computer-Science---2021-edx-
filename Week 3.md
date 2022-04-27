### Lecture 3 (CS50: Introduction to Computer Science)

**Algorithm Criteria**
1. Efficiency (Running Time, *big-O notation*)
2. Redundancy
3. Easiness to be understood
4. Correctness
5. Design

**Types**
1. Linear
2. Binary
3. Logarithm-2 (Divide & Conquer)

**Big-O Notation**
1. O(n)
2. O(1)
3. O(n^2)
4. O(n log n)
5. O(log n)
- Big O describes the upper-bound, Omega describes the lower-bound
- Circle with line is meaning O is equivalent to Omega

**Linear Search** is used when randomly scrambled data but you must make it correct. It is an *O(n)* and ω(1) (if it is your first found) algorithm.

**Binary Search (Divide & Conquer)** used when the data is arranged from small to big and start from the middle and divide. It is O(log(n)) and ω(1).

**Define Your Own Datatype**
```
typedef struct // this is an unusual data type
{
  string name;
  string number;
}
person; // datatype name

// in the main code
person people[2];

people[0].name = "Carter";
people[0].number = "+016-4859110";

people[1].name = "David";
people[1].number = "+012-4856110"

```
- by doing so, the data is *encapsulated (contained)* inside a container

**Sorting Algorithm**
1. Selection Sort
  - check the index of the smallest by comparison and move it to one index
  - running time is O(n<sup>2</sup>) and ω(n<sup>2</sup>)
2. Bubble Sort
  - running time is O(n<sup>2</sup>) and ω(n)
  - swap only the nearest number by comparison and loops it

**Recursions**: A functions calling itself but must define the base case within the limitation of the computer memory.

**Merge and Sort**, is based on comparison of two sorted list, with the spirit of *Recursion* and O(log(n)) and ω(nlog(n)) running time but it uses more memory. 
