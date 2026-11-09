# GPU computing in Jupyter4NFDI

## Learning objectives

By the end of this lesson, you will be able to:

- explain what a graphics processing unit (GPU) does;
- identify research tasks that may benefit from one;
- be aware what  GPU resources offered by Jupyter4NFDI;
- recognise when a CPU is the better option.

## What is a GPU?

A typical laptop or desktop computer uses a CPU (Central Processing Unit, most commonly called a "processor"), which is designed to execute a wide variety of instructions, including tasks involving complex decision-making. CPUs are particularly good at sequential processing.

A GPU (Graphics Processing Unit) is designed to perform many similar numerical operations in parallel. GPUs were first developed for graphics, but are also useful for scientific computing and machine learning.


## Examples of using GPU in research:

- analysing large collections of images or microscopy data;
- accelerating selected simulation and numerical methods;
- parallel processing of scientific data using GPU-enabled libraries.

**Not everything runs faster on a GPU.** Reading files, network requests, many small calculations and code with complicated sequential logic may run just as fast or faster on a CPU. For example, a GPU does not automatically accelerate ordinary Python code: it must be written using GPU-capable software such as PyTorch.

## GPUs on Jupyter4NFDI

Jupyter4NFDI offers GPU-capable server profiles, but **access requires approval** and resources are limited. GPU-enabled nodes are shared and offered on a first-come, first-served basis.

| Cloud | Advertised GPU profile | Host RAM | Virtual CPUs | Resource-sharing approach |
| --- | --- | --- | --- | --- |
| JSC-Cloud | NVIDIA A100 80 GB PCIe | 8 GB | 2 | NVIDIA Multi-Instance GPU (MIG) |
| deNBI-Cloud | NVIDIA Tesla V100 PCIe 16 GB | 8 GB | 2 | Time-slicing |

**Important:** The model name and its advertised physical GPU memory do **not** necessarily mean the full physical GPU or its full memory is available exclusively to your session. The A100 uses MIG partitioning, while the V100 uses time-slicing. Check the memory and device actually visible to your job. The **8 GB RAM** in the table refers to system memory, not GPU memory.

Resources and profiles can change. See the [current GPU access documentation](https://nfdi-jupyter.de/users/gpu-access/) before submitting a request.


**Next:** [Requesting GPU access](02_request_access.md).
