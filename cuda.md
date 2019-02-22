# Notes on the book: "Professional CUDA C programming" by J. Cheng, etc.  
# Definitions
---
*Latency* is the time that needed to start and complete an operation.  
*Bandwidth* is the amount of data that can be processed per unit of time.  
*Throughput* is the amount of operations that can be processed per unit of time.  
*Heterogeneous Architecture* consists of several CPUs (called *host*) and several GPUs (called *device*).  
*CUDA* is a general purpose parallel computing platform and programming model. CUDA platform is accessible through the extension of programming languages e.g. CUDA C.

## Notes

GPU *capability* described by:

* '#' of CUDA cores
* Memory size  

GPU *performance* described by:

* Peak computation performance (usually in Tflops)
* Memory Bandwidth (Gb/s)

CPUs are good for control-intensive tasks GPUs are good for data-parallel computation-intensive tasks.

Thread CPU vs GPU:
* CPU's threads are heavyweight. 16 or 32 threads can run concurrently. Goal: minimize latency.
* GPU's threads are lightweight. Up to 1,536 threads can run concurrently on each processor. GPUs have many processors. Goal: maximize throughput.

For *host memory* use variable names started with "h\_" and for *device memory* use "d\_".
