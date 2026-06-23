# Parallel Matrix Multiplication in Python 🚀

## 📌 Overview
This project explores and optimizes matrix multiplication using various **parallel programming techniques in Python**. It compares sequential and parallel approaches to evaluate performance improvements and scalability on multi-core systems.

The project includes:
- Multiple parallel implementations
- Performance benchmarking and visualization
- A user-friendly GUI for running experiments

---

## 🎯 Objectives
- Implement matrix multiplication using different techniques
- Analyze performance across methods
- Compare results with optimized NumPy baseline
- Explore parallelism in Python (threads vs processes)
- Visualize results interactively using a GUI

---

## 🧠 Implemented Techniques

### ✅ Baselines
- **Naive Sequential Implementation**
- **NumPy Optimized (np.dot)**

### ⚡ Parallel Methods
- Multithreading (`threading`)
- Multiprocessing (`multiprocessing.Pool`)
- Process Pools (`concurrent.futures`)
- Shared Memory Multiprocessing
- Blocked Matrix Multiplication
  - Sequential Blocked
  - Parallel Blocked (Shared Memory)

---

## 🏗️ System Architecture

The system follows a modular design:

- **MatrixMultiplication Class** – Core computation engine  
- **Config Class** – Handles experiment parameters  
- **SharedMemoryRegistry** – Manages shared memory lifecycle  
- **Benchmark Module** – Evaluates performance  
- **GUI (Tkinter)** – Interactive interface  

---

## 📊 Performance Analysis

The system evaluates:
- Execution Time
- CPU Utilization
- Speedup vs NumPy baseline

### Key Findings:
- ✅ NumPy remains the fastest (due to C/Fortran optimizations)
- ⚠️ Multiprocessing introduces overhead (IPC, serialization)
- ⚠️ Multithreading limited by Python GIL
- ✅ Shared memory improves multiprocessing efficiency but still slower than NumPy
- ✅ Parallel methods scale in CPU usage but not always in speed

---

## 🖥️ GUI Features

- Configure matrix size and workers
- Select multiplication methods
- Run benchmarks interactively
- Visualize matrices and results
- Real-time logging and progress tracking

---

## 🛠 Technologies Used

- Python 3
- NumPy
- Matplotlib
- Tkinter
- multiprocessing / threading
- concurrent.futures
- psutil
- pytest
