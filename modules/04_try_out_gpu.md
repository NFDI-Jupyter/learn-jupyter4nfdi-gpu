# Try some a GPU-enabled code

## Learning objectives

- Run sample Python code using GPU

## 1. Test the Python environment

In a Python notebook:

```python
try:
    import torch
except ImportError:
    print("PyTorch is not installed in this kernel.")
else:
    print("PyTorch version:", torch.__version__)
    print("CUDA available:", torch.cuda.is_available())
    if torch.cuda.is_available():
        print("Visible GPU:", torch.cuda.get_device_name(0))
```
A machine with a visible GPU can still report `False` if the current Python environment lacks a compatible CUDA-enabled PyTorch build. The **Jupyter kernel** and its packages matter; choosing a GPU server alone is not enough. Avoid installing or replacing large packages blindly—first check which GPU-capable environments are available.

## 2. Run a real GPU calculation

If `torch.cuda.is_available()` returns `True`, run this code:

```python
import torch

device = torch.device("cuda")
a = torch.randn((1024, 1024), device=device)
b = torch.randn((1024, 1024), device=device)
c = a @ b

torch.cuda.synchronize()  # Wait for queued operations to finish
print("Result device:", c.device)
print("Example result:", float(c[0, 0]))
```
