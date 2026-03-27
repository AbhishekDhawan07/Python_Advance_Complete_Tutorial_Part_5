# 🐍 Python_Advance_Complete_Tutorial_Part_5

> **A comprehensive, hands-on collection of advanced Python tutorials** — Part 5 focuses entirely on mastering sorting algorithms from first principles, covering multiple implementation strategies with time complexity analysis for each.

---

## 📁 Repository Structure

```
Python_Advance_Complete_Tutorial_Part_5/
└── All Major Sorting Algorithms in Python/
    └── All Major Sorting Algorithms.ipynb
```

---

## 📌 Table of Contents

1. [About This Repository](#-about-this-repository)
2. [About This Folder](#-about-this-folder)
3. [About the Notebook](#-about-the-notebook)
4. [Algorithms Covered](#-algorithms-covered)
   - [Selection Sort](#1-selection-sort)
   - [Insertion Sort](#2-insertion-sort)
   - [Bubble Sort](#3-bubble-sort)
   - [Quick Sort](#4-quick-sort)
   - [Merge Sort](#5-merge-sort)
5. [Complexity Summary Table](#-complexity-summary-table)
6. [Prerequisites](#-prerequisites)
7. [How to Run](#-how-to-run)
8. [Learning Approach](#-learning-approach)
9. [Who Is This For?](#-who-is-this-for)
10. [License](#-license)

---

## 📖 About This Repository

`Python_Advance_Complete_Tutorial_Part_5` is part of a multi-series Python tutorial repository designed to take learners beyond the basics. Each part targets a specific domain of advanced Python programming.

**Part 5** dives deep into **sorting algorithms** — one of the most fundamental topics in computer science and software engineering interviews. Rather than offering just one textbook implementation per algorithm, this part demonstrates **multiple methods** per algorithm, progressively improving efficiency and addressing real-world edge cases.

---

## 📂 About This Folder

**Folder:** `All Major Sorting Algorithms in Python`

This folder contains a focused study of the five most important comparison-based sorting algorithms in Python. Each algorithm is broken down into multiple implementation variants — from the naive baseline to optimized production-quality approaches — all within a single interactive notebook.

---

## 📓 About the Notebook

**File:** `All Major Sorting Algorithms.ipynb`

This Jupyter Notebook is structured as an interactive coding tutorial. Each algorithm section begins with a **plain-English explanation** of what the algorithm does, followed by **multiple Python implementations** ranging from basic to advanced. Every code cell includes:

- Inline comments explaining each step
- Big-O time complexity annotations in the heading
- A test array with printed expected output for immediate verification

---

## 🔢 Algorithms Covered

### 1. Selection Sort

> Finds the minimum element repeatedly and places it at the correct position.

| Method | Description | Complexity |
|--------|-------------|------------|
| **Method 1** — Basic Selection Sort | Standard approach: find minimum in unsorted part, swap with first unsorted element | O(n²) |
| **Method 2** — Selection Sort with Early Exit | Skips the swap if the element is already in the correct position — reduces unnecessary writes | O(n²) but fewer swaps |
| **Method 3** — Bidirectional Selection Sort (Cocktail Selection) | Finds both minimum AND maximum in each pass, placing both at correct ends simultaneously — halves the number of passes | O(n²) fewer passes |

---

### 2. Insertion Sort

> Builds the sorted array one element at a time by inserting each element into its correct position.

| Method | Description | Complexity |
|--------|-------------|------------|
| **Method 1** — Basic Insertion Sort | Compare each element with previous ones and shift until correct position is found | O(n²) |
| **Method 2** — Insertion Sort with Binary Search | Uses `bisect` to find the correct position — reduces comparisons from O(n) to O(log n) per element | O(n log n) comparisons, O(n²) shifts |
| **Method 3** — Shell Sort (Improved Insertion Sort) | Runs insertion sort with a large gap first, then reduces the gap — elements travel in larger steps to reach correct position faster | O(n log² n) |

---

### 3. Bubble Sort

> Repeatedly compares adjacent elements and swaps them if they are in the wrong order. Largest elements bubble up to the end.

| Method | Description | Complexity |
|--------|-------------|------------|
| **Method 1** — Basic Bubble Sort | Classic approach — always runs all passes regardless of whether the array is already sorted | O(n²) |
| **Method 2** — Optimized Bubble Sort with Early Exit | Adds a `swapped` flag to detect if no swap happened in a pass — if no swap, the array is already sorted and iteration stops early | O(n) best case |

---

### 4. Quick Sort

> Picks a pivot, partitions the array around it (smaller left, larger right), then recursively sorts both halves.

| Method | Description | Complexity |
|--------|-------------|------------|
| **Method 1** — Basic Quick Sort (Last Element as Pivot) | Always picks the last element as pivot — fast in practice but degrades on already-sorted arrays | O(n²) worst case |
| **Method 2** — Quick Sort with Random Pivot | Randomly selects the pivot before each partition — avoids worst-case on sorted/reverse-sorted arrays | O(n log n) expected |
| **Method 3** — Quick Sort with Median-of-Three Pivot | Picks the median of first, middle, and last elements as pivot — much better pivot choice without random number overhead | O(n log n) better pivot |

---

### 5. Merge Sort

> Divides the array into two halves, recursively sorts each half, then merges them back in sorted order.

| Method | Description | Complexity |
|--------|-------------|------------|
| **Method 1** — Basic Merge Sort | Classic top-down recursive approach — always O(n log n) regardless of input | O(n log n) always |
| **Method 2** — Merge Sort with Early Skip | Before merging, checks if `arr[mid] <= arr[mid+1]` — if true, both halves are already in order and merge is skipped entirely | O(n log n), faster on nearly-sorted data |
| **Method 3** — Bottom-Up Iterative Merge Sort | Starts merging pairs of size 1, then size 2, then size 4... eliminates recursion stack, saving O(log n) stack space | O(n log n), no recursion stack |

---

## 📊 Complexity Summary Table

| Algorithm | Best Case | Average Case | Worst Case | Space | Stable? |
|-----------|-----------|--------------|------------|-------|---------|
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | ❌ No |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ Yes |
| Shell Sort | O(n log n) | O(n log² n) | O(n²) | O(1) | ❌ No |
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ No |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ Yes |

---

## ✅ Prerequisites

Before running this notebook, make sure you have the following:

- **Python 3.7+**
- **Jupyter Notebook** or **JupyterLab**

  ```bash
  pip install notebook
  ```

- **Standard Library only** — this notebook uses only Python built-ins (`bisect`, `random`). No third-party packages are required.

---

## ▶️ How to Run

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/Python_Advance_Complete_Tutorial_Part_5.git
   ```

2. **Navigate to the folder:**

   ```bash
   cd "Python_Advance_Complete_Tutorial_Part_5/All Major Sorting Algorithms in Python"
   ```

3. **Launch Jupyter Notebook:**

   ```bash
   jupyter notebook "All Major Sorting Algorithms.ipynb"
   ```

4. **Run cells interactively** — press `Shift + Enter` to execute each cell and observe the output.

---

## 🧠 Learning Approach

This notebook follows a **progressive learning model**:

```
Basic Implementation
        ↓
  Identify Weakness
        ↓
  Optimized Variant
        ↓
  Advanced Variant
```

Each algorithm is taught by first showing the simplest correct solution, then identifying its weaknesses (unnecessary swaps, worst-case pivots, recursion depth), and finally presenting cleaner, faster alternatives — so you understand *why* each optimization matters, not just *what* it does.

---

## 🎯 Who Is This For?

- **Students** preparing for data structures and algorithms coursework
- **Developers** brushing up on fundamentals for technical interviews
- **Python enthusiasts** wanting to understand performance trade-offs in sorting
- **Anyone** who wants to go beyond `list.sort()` and understand what happens under the hood

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute for educational purposes.

---

> 💡 **Tip:** Try modifying the test arrays in each cell to include edge cases — empty arrays, single elements, already-sorted arrays, and reverse-sorted arrays — to see how each algorithm behaves!
