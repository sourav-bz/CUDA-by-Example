# CUDA-by-Example-source-code-for-the-book-s-examples-
CUDA by Example, written by two senior members of the CUDA software platform team, shows programmers how to employ this new technology.  The authors introduce each area of CUDA development through working examples. 

# Getting Started

## Prerequisites

Before running the CUDA examples, ensure you have the following installed:

1. **NVIDIA GPU** with CUDA support
2. **CUDA Toolkit** (version 11.0 or later recommended)
3. **NVIDIA drivers** compatible with your CUDA version

### Check CUDA Installation

Verify your CUDA installation by running:
```bash
nvcc --version
```

You should see output similar to:
```
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2022 NVIDIA Corporation
Built on Wed_Sep_21_10:33:58_PDT_2022
Cuda compilation tools, release 11.8, V11.8.89
```

## How to Compile and Run Examples

### Basic Compilation

Navigate to the chapter directory containing the CUDA source file and compile:

```bash
cd chapter03
nvcc -o program_name source_file.cu
```

### Running the Examples

After compilation, run the executable:

```bash
./program_name
```

## Example: Running enum_gpu.cu

The `enum_gpu.cu` program displays detailed information about your CUDA devices:

```bash
# Navigate to chapter03 directory
cd chapter03

# Compile the program
nvcc -o enum_gpu enum_gpu.cu

# Run the program
./enum_gpu
```

This will output information about your GPU including:
- Device name and compute capability
- Memory specifications
- Multiprocessor details
- Thread and block limits

### Sample Output

```
   --- General Information for device 0 ---
Name:  NVIDIA GeForce RTX 3050 Laptop GPU
Compute capability:  8.6
Clock rate:  1740000
Device copy overlap:  Enabled
Kernel execution timeout :  Enabled
   --- Memory Information for device 0 ---
Total global mem:  4084137984
Total constant Mem:  65536
Max mem pitch:  2147483647
Texture Alignment:  512
   --- MP Information for device 0 ---
Multiprocessor count:  16
Shared mem per mp:  49152
Registers per mp:  65536
Threads in warp:  32
Max threads per block:  1024
Max thread dimensions:  (1024, 1024, 64)
Max grid dimensions:  (2147483647, 65535, 65535)
```

## Common Compilation Options

- **Debug mode**: `nvcc -g -G -o program_name source_file.cu`
- **Optimization**: `nvcc -O3 -o program_name source_file.cu`
- **Specify architecture**: `nvcc -arch=sm_86 -o program_name source_file.cu`

## Troubleshooting

1. **"nvcc: command not found"**: Install CUDA Toolkit
2. **"CUDA driver version is insufficient"**: Update NVIDIA drivers
3. **Compilation errors**: Check that all required header files are in the correct paths

#Table of Contents

- Why CUDA? Why Now?
- Getting Started
- Introduction to CUDA C
- Parallel Programming in CUDA C
- Thread Cooperation
- Constant Memory and Events
- Texture Memory
- Graphics Interoperability
- Atomics
- Streams
- CUDA C on Multiple GPUs
- The Final Countdown


#Authors

Jason Sanders is a senior software engineer in NVIDIA's CUDA Platform Group, helped develop early releases of CUDA system software and contributed to the OpenCL 1.0 Specification, an industry standard for heterogeneous computing. He has held positions at ATI Technologies, Apple, and Novell.

Edward Kandrot is a senior software engineer on NVIDIA's CUDA Algorithms team, has more than twenty years of industry experience optimizing code performance for firms including Adobe, Microsoft, Google, and Autodesk.




![CUDA-by-Example](https://github.com/CodedK/CUDA-by-Example-source-code-for-the-book-s-examples-/blob/master/Pearson_CUDA_BookCover.jpg)


https://developer.nvidia.com/cuda-example
