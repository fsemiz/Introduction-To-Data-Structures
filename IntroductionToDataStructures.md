# Introduction to Data Structures

Authors: **Fatih Semiz - Kaan Keskin**

Date: July 2021

Available at (Source): https://github.com/fsemiz/Introduction-To-Data-Structures

Available at (Forked): https://github.com/kaan-keskin/Introduction-To-Data-Structures

Java Collections Framework Benchmark Tool: https://github.com/kaan-keskin/java-collections-benchmark

**Resources:**

- Introduction to Algorithms - Cormen, Leiserson, Rivest, Stein
- Algorithms - Sanjoy Dasgupta, Christos Papadimitriou, Umesh Vazirani
- Data Structures and Algorithms with Python - Kent D. Lee, Steve Hubbard
- Grokking Algorithms - Aditya Y. Bhargava
- Wikipedia - www.wikipedia.com

## Introduction
To solve a problem in the world of computer science and normal life, we must first make a plan and determine the solution steps. This can be likened to looking at a recipe before cooking. To make a computer perform a task, we need to provide more details. Technically speaking an algorithm can be defined as the following: "Finite sequence of instructions to perform a specific task in a finite amount of time". The basis of creating a good algorithm for many problems lies in storing the data to be used appropriately and efficiently. By saying efficient we generally talk about **accessing**, **insertion**, **deletion**, **searching**, and **sorting** the data. These operations complexities are directly related to which container is used to store that data.

| <img src="./images/Algorithm.jpg" alt="Algorithm" style="zoom:50%;" /> |
|:--:|
| *Retrieved from https://www.techidence.com/whats-an-algorithm-understand-how-it-works-in-apps-and-websites/* |

To put it briefly, data structures are containers used to store data. However, each data structure is generally built to store a certain type of data. A data structure may be efficient in some operations but inefficient in other operations, and this is often the case. For this reason, we must choose data structures in accordance with the data at hand. For example, if you try to drink a soup with a fork, it will take you quite a while to finish it. However, if you use a spoon for soup and a fork for pasta, you will see that you can eat both fast this time. The purpose of this session will be to go over the topics of data structures as well as to remind you where and what type of data structures are used in which situation.

| <img src="./images/SoupWithFork.jpg" alt="Soup with fork" style="zoom:67%;" /> |
| :----------------------------------------------------------: |
| *Retrieved from https://www.linkedin.com/pulse/eating-soup-forks-michael-henderson/* |

## Basic Data Structures: Arrays and Linked Lists

### Array Data Structure

    Array: Contiguous area of memory consisting of equal-size elements indexed by contiguous integers.

In computer science, an array data structure, or simply an array, is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key. An array is stored such that the position of each element can be computed from its index tuple by a mathematical formula. The simplest type of data structure is a linear array, also called one-dimensional array. 

The key point about an array is we have constant time access to read and write.

    constant_time_access = array_addr + element_size x (i - first_index)

For example, an array of 10 32-bit (4-byte) integer variables, with indices 0 through 9, may be stored as 10 words at memory addresses 2000, 2004, 2008, ..., 2036, (in hexadecimal: 0x7D0, 0x7D4, 0x7D8, ..., 0x7F4) so that the element with index i has the address 2000 + (i × 4).

| ![Array Example](./images/array-example.png) |
|:--:|
| *Retrieved from https://beginnersbook.com/2018/10/data-structure-array/* |

The memory address of the first element of an array is called first address, foundation address, or base address.

**Arrays are among the oldest and most important data structures, and are used by almost every program. They are also used to implement many other data structures, such as lists and strings.** 

They effectively exploit the addressing logic of computers. In most modern computers and many external storage devices, the memory is a one-dimensional array of words, whose indices are their addresses. Processors, especially vector processors, are often optimized for array operations.

**Arrays are useful mostly because the element indices can be computed at run time. Among other things, this feature allows a single iterative statement to process arbitrarily many elements of an array.** 

**For that reason, the elements of an array data structure are required to have the same size and should use the same data representation.** 

The set of valid index tuples and the addresses of the elements (and hence the element addressing formula) are usually, but not always, fixed while the array is in use.

**The term array is often used to mean array data type, a kind of data type provided by most high-level programming languages that consists of a collection of values or variables that can be selected by one or more indices computed at run-time. Array types are often implemented by array structures; however, in some languages they may be implemented by hash tables, linked lists, search trees, or other data structures.**

#### Times for Common Operations

| Location | Add | Remove |
| :--: | :--: | :--: |
| Beginning | O(n) | O(n) |
| End | O(1) | O(1) |
| Middle | O(n) | O(n) |

**AddEnd**: We just add it, then update the number of elements that are in use. That's an O(1) operation.

**RemoveEnd**: As well, that's an O(1) operation. Because we just update the number of elements that are in use.

**RemoveBeginning**: Where it's get to be expensive, if we want to remove the first element. So we remove the first element, then we need to move all elements to the left (or down). That's an O(n) operation.

**AddBeginning**: I we want to insert at the beginning, we need to move every element to the right (or up), then insert the element at the beginning.

Arrays are great if you want to add or remove element at the end. But it's expensive if you want to add or remove in the middle or at the beginning.

However, a huge advantage for arrays is that we have constant time access to elements either read or write.


