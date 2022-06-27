Preaparing:
- Ubuntu machine v14.0.4
  - Install Vim, Git, Cscope, Screen 
  - Using MobaXterm for SSH

# Section 1: Introduction
# Section 2: Understand Headers Files
## 7. What are Header Files and their Purpose?
## 8. Relationship between Source and Header Files
## 9. Text Substitution
# Section 3: Preprocessing Directives
## 12. Problem Of Duplicate Inclusion of Header Files
## 13. What are Pre-processing Directives ?
* Before Compiler actually compiles the source file, it performs the text substitution 
* The C preprocessor directives (#include, #define) is just a simple text substitution tool
* Text Substitution is performed first before the compiler actually starts compilation of source files.
* Directives can be written in both - Source files as well as Header files



# Index
```
Curriculum :

**********************************************

Release 1 Building and Managing a Library

**********************************************

Section 1 : Introduction to Libraries

    What is Library

    Relationship between Library and Application

    Ex : Doubly linked list as a Library

    Quick Compilation Steps

    Summary

Section 2 : Header Files

    Relationship between Source and header files

    Text Substitution Method

    Text Substitution Method - Example and Demo

Section 3 : Preprocessing Directives

    Problem of Duplicate inclusion of Hdr files

    Pre-processing Directives

    Solution to Duplicate inclusion of Hdr files

Section 4 : Correct way of Using Structures and Functions

    Structures - Define and Use thumb Rule

    Functions - Declare and Use thumb rule

    The problem of Recursive Dependency

    A solution to Recursive Dependency

Section 5 : Creation of Static and Dynamic Libraries

    Resuming with Doubly Linked List Library

    Quick Creation of Static and Dynamic Libraries

    Linking with Static Library

    Linking with Dynamic Library

Section 7: Understanding four stages of Compilation

    Four stages of C/C++ Compilation

    How Dynamic Library works ?

    Dynamic Linking : Linking with Dynamic Library

    Comparison - Static Vs Dynamic Linking

Section 8 : Building using a Makefile

    What are Makefiles and why do we need it

    Functions of Makefile

    Makefile Dependency tree

    Steps of Writing a Makefile

    Assignment on Makefile

Section 9 : Run-time Programmable libraries

    What are Programmable Libraries?

    Steps to Program the libraries

    Registering of the callbacks with Libraries

        key_match callback

        comparison_fn callback

    Delegation of Application-specific operations to Libraries

Section 10 : Writing Iterators using Macros

    What are Iterative Macros ?

    Why we need Iterative Macros ?

    How to Write Iterative Macros - For Trees and Linked Lists

    Exercises

Section 11 : Glue Based Libraries and Data structures

    What are the Glue Based Libraries?

    Introducing Glthreads - A Glued LinkedList

    Glthreads Vs Traditional Linked List

    Structure field offset

    GLThread Operations

    Code Walk

    GLThread Benefits  

Section 12 : Bit Level Programming

    Logical Operators

    Implementing BIT manipulating C macros

    ```c
    #define SET_BIT(n, BIT_F) # BIT_F is 2^x
        (n |= BIT_F)
    #define UNSET_BIT(n, BIT_F)
        (n &= ~BIT_F)
    #define IS_SET_BIT(n, BIT_F)
        (n & BIT_F)
    ```

    Using Enums as Bits

    Bit Pattern Matching

    BitMaps
Assignment instructions
120 minutes to complete
5 student solutions

Follow the instructions as given in Question.
Questions for this assignment
Bit programming Questions and Assignments.
Q1. Create a file bitsop.h and write the implementation of below macros.
bitsop.h #include stadint.h file.
Assume n is uint32_t type integer. bit is any number in power of 2 not exceeding 2 ^ 31.
LSB is designated as 0th bit, and MSB as 31st bit.
1. Write a function which print the bit pattern of a uint32_t number n.
For example, if n = 40, then output should be 0010 1000
void print_bit_pattern(uint32_t n).
Note : use above fn to verify the solution of correctness of subsequent questions.
2. Must set xth bit in number n, where bit = 2 ^ x.
#define SET_BIT(n, bit)
3. Must unset xth bit in number n, where bit = 2 ^ x.
#define UNSET_BIT(n, bit )
4. MUST return TRUE or FALSE depending on xth bit is set or not.
#define  IS_BIT_SET(n, bit)
5. Must Toggle xth bit in number not
#define TOGGLE_BIT(n, bit)
6. must compute the complement of number n. n itself should not get modified.
#define COMPLEMENT(n)
7. fn which returns number of bits set in uint32_t number n.
For example, for n = 40, it should return 2 because binary of 40 is 0010 1000
uint8_t count_bit_set(uint32_t n);
8. Rotate the bit pattern of number n by k units towards right.
For example, if n = 40 , binary = 0010 1000 and if k = 4, then resultatnt bit pattern should be 1000 0010 ( i have ignored number of leading consecutive zeros in binary bit pattern in the example, but those are there )
9. Given an IP Address and a mask value - 20.1.1.2/24. Apply the Mask on IP Address and print the bit pattern of resultant ip address obtained.
10. Given a 32 bit integer, and two integers p and q such that 0 <= p < q <= 31, which represent bit positions, print equivalent integer formed by bits in interval [p, q] (p, q inclusive) and remaining bits set to zero.
11. Test whether the integer n is a power of two or not ?
bool isPowerOfTwo(uint32_t n);
Browse Internet, search for more bit programming Questions and do them.

1. Bit programming Questions and Assignments.
Q1. Create a file bitsop.h and write the implementation of below macros.
bitsop.h #include stadint.h file.
Assume n is uint32_t type integer. bit is any number in power of 2 not exceeding 2 ^ 31.
LSB is designated as 0th bit, and MSB as 31st bit.
1. Write a function which print the bit pattern of a uint32_t number n.
For example, if n = 40, then output should be 0010 1000
void print_bit_pattern(uint32_t n).
Note : use above fn to verify the solution of correctness of subsequent questions.
2. Must set xth bit in number n, where bit = 2 ^ x.
#define SET_BIT(n, bit)
3. Must unset xth bit in number n, where bit = 2 ^ x.
#define UNSET_BIT(n, bit )
4. MUST return TRUE or FALSE depending on xth bit is set or not.
#define  IS_BIT_SET(n, bit)
5. Must Toggle xth bit in number not
#define TOGGLE_BIT(n, bit)
6. must compute the complement of number n. n itself should not get modified.
#define COMPLEMENT(n)
7. fn which returns number of bits set in uint32_t number n.
For example, for n = 40, it should return 2 because binary of 40 is 0010 1000
uint8_t count_bit_set(uint32_t n);
8. Rotate the bit pattern of number n by k units towards right.
For example, if n = 40 , binary = 0010 1000 and if k = 4, then resultatnt bit pattern should be 1000 0010 ( i have ignored number of leading consecutive zeros in binary bit pattern in the example, but those are there )
9. Given an IP Address and a mask value - 20.1.1.2/24. Apply the Mask on IP Address and print the bit pattern of resultant ip address obtained.
10. Given a 32 bit integer, and two integers p and q such that 0 <= p < q <= 31, which represent bit positions, print equivalent integer formed by bits in interval [p, q] (p, q inclusive) and remaining bits set to zero.
11. Test whether the integer n is a power of two or not ?
bool isPowerOfTwo(uint32_t n);

bitops.h ->

#include <stdint.h>

#include <stdio.h>

#include <stdlib.h>

#include <sys/types.h>


#define SET_BIT(n, bit) {\

n |= 1 << bit;}


#define UNSET_BIT(n, bit) {\

n &= ~(1 << bit);}


#define IS_SET_BIT(n, bit) {\

printf("%s\n", (n & (1 << bit))? "True" : "False"); \

}


#define TOGGLE_BIT(n, bit) {\

n ^= 1 << bit;}


#define COMPLEMENT(n) ({int c = ~n;c;})

bitpatt.c ->

#include "bitsops.h"


uint32_t rotate_bits_to_right(uint32_t n, uint8_t k)

{

    while (k != 0) {

        if(n & (1 << 0)) {

            n = n >> 1;

            n |= (1 << 31);

        } else {

            n = n >> 1;

        }

        k--;

    }


    return n;

}


uint8_t count_bit_set(uint32_t n)

{

    uint8_t count = 0;

    for (uint32_t i = 1 << 31; i > 0; i = i / 2) {

        (n & i) ? count++ : count;

    }


    return count;

}



void print_bit_pattern(uint32_t n)

{

    uint32_t count = 1;

    for (uint32_t i = 1 << 31; i > 0; i = i / 2) {

        (n & i) ? printf("1") : printf("0");


        if ((count % 4) == 0) {

            printf(" ");

        }


        count++;

    }


    printf("\n");

}


void main(int argc, char *argv[])

{

    if (argc != 2) {

        printf("Please provide a valid integer input\n");

        return;

    }


    int comp_of_n, rot_no;


    int n = atoi(argv[1]);

    print_bit_pattern(n);

    SET_BIT(n, 7);

    print_bit_pattern(n);

    UNSET_BIT(n, 7);

    print_bit_pattern(n);

    TOGGLE_BIT(n, 7);

    print_bit_pattern(n);

    comp_of_n = COMPLEMENT(n);

    print_bit_pattern(comp_of_n);

    IS_SET_BIT(n, 7);

    IS_SET_BIT(comp_of_n, 7);

    printf("Bits set in n: %d comp_of_n: %d\n", count_bit_set(n), count_bit_set(comp_of_n));

    rot_no = rotate_bits_to_right(n, 4);

    print_bit_pattern(rot_no);

}
************************************************

Release 2 Memory Management Concepts

************************************************

Section 13 : Memory Layout of Linux Process

    Virtual Memory Basics 

    Memory Layout of Linux Process 

    Example: Memory Layout of Linux Process 

    Exercise on size command  

Section 14 : Stack Memory Management

    Stack Memory Basics and Contents 

    Stack-Overflow and Prevention 

    Stack Memory Corruption 

    Common Cpu Registers

    Procedure Call Mechanism - Step by Step

    Purpose of Base Pointer register (ebp) 

    Procedure Return Mechanism - Step by Step

    Lab session  

Section 15 : Heap Memory Management

    Introduction and Goals

    How Malloc Works

    Top of Heap Memory region - break pointer

    Heap Memory Mgmt Sys Calls - brk and sbrk

    Meta and Data Blocks

    How free() works

    Block Splitting

    Block Merging

    Memory Illness - Problem of Fragmentation

Section 16 : Concept of Paging

    Introduction to Paging

    Byte Addressable Memory

    32 bit and 64 bit Machine Architecture

    Address Bus and Data bus         

    Physical Vs Virtual Address

    Physical Memory Frames        

    Virtual Address Composition

    Page Table

    Paging In Action

    Shared Physical Memory

Section 17 : Multilevel Paging

Section 18 : Demand Paging

Section 19 : Memory Management for Multi-threaded Process



The intention of this course is to make you ready for System programming Technical interviews from beginners to upto 8-9 yrs of experience.


Q. What are the frequently asked questions by interviewers in a technical round when someone writes C/C++/System Programming language on their resume?

Answer : If i am interviewer, what questions i would ask depends on his no of years of experience in C.

1–3 yrs of experience — I would have asked:

    Double pointers

    design a Macro to return the size of the structure

    Two Dimensional Arrays, passing and returning arrays from a fn

    Different stages of C program compilation

    how fork() works

    What are various ways to debug memory corruptions.

    various IPCs

    Heap and Stack memory-based Question

4–6 yrs of experience - I would have asked:

    How memory is allocated by the OS

    Internal and external fragmentation, what can be done to avoid it

    System calls, strace()

    Trade-of of one IPC over other

    various ways to communicate with kernel and comparison

    Data (De)Serialization in C

    RPC in C

    callbacks advanced application

    typedef Vs #define

    Generic programming in C using macros

    Thread Synchronization

    Heap and Stack memory-based Question

7+ yrs of experience - I would have asked

    Have you designed any system module to solve any problem

    Design thread library 0 what functionalities would you incorporate in and how?

    What are Dos and Dont’s for writing a robust and flexible library

    How to write generic code in C

    Various ways to implement timers in C, and comparison of approaches

    How do Interrupts work ?

    IPCs and comparison

    How would you convert a C code to C++ and vice versa

    How to write a tool to detect memory leaks Or garbage collection

    Design your own memory allocation tool. Why would you write your own memory allocation scheme?

    When to go for Multi-process design over Multi-threaded design and vice versa

    How ValGrind tool works

    In production code, would you favor recursive but simple logic, Or Nonrecursive but complex logic, and why?

If you analyze the pattern,

Candidate with 1–3 yrs of experience, I would choose to ask more of a direct and straightforward Questions.

Candidate with 4–6 yrs of experience, I would choose to ask more advanced technical C Question plus some comparison of approaches based Questions

Candidate with 7+ yrs of experience, I would choose to ask more of a design and Analysis based Question.
```