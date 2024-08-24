# Memory Allocation Strategies

This project demonstrates the implementation of various memory allocation strategies used in operating systems, including **First Fit**, **Best Fit**, and **Worst Fit** algorithms. The purpose of these algorithms is to allocate memory blocks to different processes in a manner that optimizes the use of available memory.

## Table of Contents
- [Memory Allocation Strategies](#memory-allocation-strategies)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Algorithms Implemented](#algorithms-implemented)
    - [1. First Fit](#1-first-fit)
    - [2. Best Fit](#2-best-fit)
    - [3. Worst Fit](#3-worst-fit)
  - [Program Details](#program-details)
  - [How to Run](#how-to-run)
  - [Example Output](#example-output)
  - [License](#license)

## Introduction

In an operating system, memory management is a crucial function that manages the allocation of blocks of memory to different processes. Contiguous memory allocation is an essential technique used in modern operating systems to allocate memory to processes. Each algorithm has its advantages and disadvantages, but all are designed to optimize memory allocation and reduce fragmentation This project focuses on three common memory allocation strategies:

1. **First Fit**: Allocates the first block that is large enough to satisfy the memory requirement.
2. **Best Fit**: Allocates the smallest block that is large enough to satisfy the memory requirement.
3. **Worst Fit**: Allocates the largest available block to satisfy the memory requirement.

These algorithms help optimize memory usage, reduce fragmentation, and ensure that processes are allocated memory in an efficient manner.

## Algorithms Implemented

### 1. First Fit

- The **First Fit** algorithm allocates the first memory block that is large enough to accommodate the process.
- It scans the memory blocks sequentially until it finds a suitable block.

### 2. Best Fit

- The **Best Fit** algorithm allocates the smallest available memory block that is large enough to accommodate the process.
- It searches for the most tightly fitting block to minimize wasted space.

### 3. Worst Fit

- The **Worst Fit** algorithm allocates the largest available memory block to the process.
- This strategy aims to reduce the fragmentation by keeping larger blocks available for future processes.

## Program Details

The program is implemented in C and demonstrates how these memory allocation strategies can be applied to a set of processes and memory blocks.

### Functions

- `implimentFirstFit(int blockSize[], int blocks, int processSize[], int processes)`: Implements the First Fit allocation strategy.
- `implimentBestFit(int blockSize[], int blocks, int processSize[], int processes)`: Implements the Best Fit allocation strategy.
- `implimentWorstFit(int blockSize[], int blocks, int processSize[], int processes)`: Implements the Worst Fit allocation strategy.

### Input
- **blockSize[]**: An array representing the sizes of available memory blocks.
- **processSize[]**: An array representing the sizes of the processes to be allocated memory.
- **blocks**: The total number of memory blocks available.
- **processes**: The total number of processes that need memory.

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/your_username/Memory-Allocation-Strategies.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Memory-Allocation-Strategies
    ```

3. Compile the program using a C compiler:
    ```bash
    gcc memory_allocation.c -o memory_allocation
    ```

4. Run the program:
    ```bash
    ./memory_allocation
    ```

## Example Output

After running the program, you will see an output similar to this:

```plaintext
First Fit:
Process No.     Process Size    Block no.
1               10              1
2               6               3
3               9               Not Allocated

Best Fit:
Process No.     Process Size    Block no.
1               10              1
2               6               3
3               9               2

Worst Fit:
Process No.     Process Size    Block no.
1               10              1
2               6               3
3               9               2
