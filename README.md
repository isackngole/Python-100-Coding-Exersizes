
# 🐍 100 Python Problems — Solutions & Tests

> A curated collection of 100 Python coding problems with clean, well-tested solutions.  
> Perfect for interview preparation, coding practice, and mastering Python fundamentals.

[![Build Status](https://github.com/your-username/100-python-problems/actions/workflows/tests.yml/badge.svg)](https://github.com/your-username/100-python-problems/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Pytest](https://img.shields.io/badge/tested%20with-pytest-0A9EDC)](https://pytest.org/)
[![Coverage](https://img.shields.io/badge/coverage-98%25-brightgreen)](https://github.com/your-username/100-python-problems)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📖 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Demo](#-demo)
- [Screenshots](#-screenshots)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Project Setup](#project-setup)
  - [Running Solutions](#running-solutions)
- [Testing](#-testing)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## ✨ Features

- **100 curated problems** covering Python fundamentals, algorithms, data structures, and interview classics.
- **Clean solutions** — every problem has a well-documented `solution.py` with type hints and docstrings.
- **Comprehensive tests** — each solution has a matching `pytest` test file.
- **Difficulty labels** — Easy, Medium, Hard.
- **Organized by topic** — strings, lists, dictionaries, sorting, searching, DP, graphs, and more.
- **Beginner-friendly** — each problem folder has its own `README.md` with examples and constraints.
- **CI-ready** — GitHub Actions runs all tests on every push.
- **Coverage reports** — track test coverage with `pytest-cov`.
- **Copy-paste ready** — use any solution directly in your own project.
- **No dependencies for solutions** — pure Python, standard library only.

---

## 🧰 Tech Stack

| Layer           | Technology                          |
|-----------------|-------------------------------------|
| Language        | Python 3.10+                        |
| Testing         | pytest, pytest-cov                  |
| Linting         | flake8, black, isort, mypy          |
| CI/CD           | GitHub Actions                      |
| Package Manager | pip + virtualenv (or uv/poetry)     |
| Documentation   | Markdown + docstrings               |

---

## 🌐 Demo

- **Live Browse:** [https://github.com/your-username/100-python-problems](https://github.com/your-username/100-python-problems)
- **Problem Index:** [Jump to index](#-problem-index)
- **CI Dashboard:** [GitHub Actions](https://github.com/your-username/100-python-problems/actions)

### Try it in 30 seconds

```bash
git clone https://github.com/your-username/100-python-problems.git
cd 100-python-problems
pip install -r requirements.txt
pytest -v
```

---

## 📸 Screenshots

| Test Output | Folder Structure | Coverage Report |
|-------------|------------------|-----------------|
| ![Tests](docs/assets/tests.png) | ![Structure](docs/assets/structure.png) | ![Coverage](docs/assets/coverage.png) |

| Solution Example | Problem README | GitHub Actions |
|------------------|----------------|----------------|
| ![Solution](docs/assets/solution.png) | ![Problem](docs/assets/problem.png) | ![CI](docs/assets/ci.png) |

---

## 🚀 Getting Started

### Prerequisites

- Python **3.10+**
- `pip` and `venv` (bundled with Python)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/100-python-problems.git
   cd 100-python-problems
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate        # macOS/Linux
   venv\Scripts\activate           # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

### Environment Variables

This project doesn't require environment variables to run.  
Optional `.env` for CI or coverage tools:

```env
PYTHONPATH=.
PYTEST_ADDOPTS=-v --cov=problems --cov-report=term-missing
```

### Project Setup

```bash
# Verify Python version
python --version    # should be 3.10 or higher

# Verify tests run
pytest -q
```

### Running Solutions

Run any solution directly:

```bash
python -m problems.001_two_sum.solution
```

Import in your own code:

```python
from problems.001_two_sum.solution import two_sum

print(two_sum([2, 7, 11, 15], 9))   # [0, 1]
```

---

## 🧪 Testing

Run the **full test suite**:

```bash
pytest -v
```

Run a **single test file**:

```bash
pytest tests/test_001_two_sum.py -v
```

Run a **single test**:

```bash
pytest tests/test_001_two_sum.py::test_two_sum_basic -v
```

Run with **coverage**:

```bash
pytest --cov=problems --cov-report=term-missing
```

Generate an **HTML coverage report**:

```bash
pytest --cov=problems --cov-report=html
open htmlcov/index.html     # macOS
start htmlcov/index.html    # Windows
```

Run **linting and type checks**:

```bash
flake8 problems/ tests/
black --check problems/ tests/
isort --check-only problems/ tests/
mypy problems/
```

---

## 📚 API Documentation

Every solution exposes **pure Python functions** you can import. Below are examples.

### Example 1: `two_sum(nums, target)`

```python
from problems.001_two_sum.solution import two_sum

two_sum([2, 7, 11, 15], 9)   # [0, 1]
two_sum([3, 2, 4], 6)        # [1, 2]
two_sum([1, 2, 3], 100)      # []
```

| Parameter | Type       | Description               |
|-----------|------------|---------------------------|
| `nums`    | `List[int]` | List of integers         |
| `target`  | `int`      | Target sum                |
| **Returns** | `List[int]` | Indices of the two numbers |

---

### Example 2: `reverse_string(s)`

```python
from problems.002_reverse_string.solution import reverse_string

reverse_string("hello")     # "olleh"
reverse_string("Python")    # "nohtyP"
```

| Parameter | Type  | Description     |
|-----------|-------|-----------------|
| `s`       | `str` | Input string    |
| **Returns** | `str` | Reversed string |

---

### Example 3: `binary_search(arr, target)`

```python
from problems.016_binary_search.solution import binary_search

binary_search([1, 3, 5, 7, 9], 5)   # 2
binary_search([1, 3, 5, 7, 9], 4)   # -1
```

| Parameter | Type       | Description           |
|-----------|------------|-----------------------|
| `arr`     | `List[int]` | Sorted list of ints   |
| `target`  | `int`      | Value to find         |
| **Returns** | `int`    | Index or `-1`         |

---

### Example 4: `fibonacci(n)`

```python
from problems.006_fibonacci.solution import fibonacci

fibonacci(0)   # 0
fibonacci(10)  # 55
```

---

## 📁 Project Structure

```text
100-python-problems/
├── problems/
│   ├── 001_two_sum/
│   │   ├── README.md          # problem statement + examples
│   │   ├── solution.py        # clean solution with docstrings
│   │   └── __init__.py
│   ├── 002_reverse_string/
│   │   ├── README.md
│   │   ├── solution.py
│   │   └── __init__.py
│   └── ... (up to 100)
├── tests/
│   ├── test_001_two_sum.py
│   ├── test_002_reverse_string.py
│   └── ... (one test file per problem)
├── docs/
│   └── assets/                # screenshots, diagrams
├── .github/
│   └── workflows/
│       └── tests.yml          # CI: run pytest on push/PR
├── requirements.txt
├── pytest.ini
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🚢 Deployment

This is primarily a **learning repository**, but you can publish it as a package or docs site.

### 1. Publish to PyPI (optional)

```bash
python -m build
python -m twine upload dist/*
```

Then anyone can install it:

```bash
pip install 100-python-problems
```

### 2. Publish Docs with GitHub Pages

```bash
pip install mkdocs mkdocs-material
mkdocs new .
mkdocs gh-deploy
```

### 3. Run in Docker

```dockerfile
# Dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["pytest", "-v"]
```

```bash
docker build -t py100 .
docker run --rm py100
```

### 4. CI with GitHub Actions

`.github/workflows/tests.yml`:

```yaml
name: Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: ["3.10", "3.11", "3.12"]
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: ${{ matrix.python-version }}
      - run: pip install -r requirements.txt
      - run: pytest -v --cov=problems
```

---

## 📚 Problem Index

<details>
<summary>Click to expand all 100 problems</summary>

| # | Problem | Difficulty | Solution |
|---|---------|------------|----------|
| 001 | Two Sum | Easy | [Link](problems/001_two_sum/) |
| 002 | Reverse String | Easy | [Link](problems/002_reverse_string/) |
| 003 | Palindrome Check | Easy | [Link](problems/003_palindrome_check/) |
| 004 | FizzBuzz | Easy | [Link](problems/004_fizzbuzz/) |
| 005 | Factorial | Easy | [Link](problems/005_factorial/) |
| 006 | Fibonacci | Easy | [Link](problems/006_fibonacci/) |
| 007 | Prime Check | Easy | [Link](problems/007_prime_check/) |
| 008 | Sum of List | Easy | [Link](problems/008_sum_of_list/) |
| 009 | Max in List | Easy | [Link](problems/009_max_in_list/) |
| 010 | Min in List | Easy | [Link](problems/010_min_in_list/) |
| 011 | Count Vowels | Easy | [Link](problems/011_count_vowels/) |
| 012 | Reverse Integer | Medium | [Link](problems/012_reverse_integer/) |
| 013 | Anagram Check | Easy | [Link](problems/013_anagram_check/) |
| 014 | Remove Duplicates | Easy | [Link](problems/014_remove_duplicates/) |
| 015 | Find Missing Number | Easy | [Link](problems/015_find_missing_number/) |
| 016 | Binary Search | Easy | [Link](problems/016_binary_search/) |
| 017 | Linear Search | Easy | [Link](problems/017_linear_search/) |
| 018 | Bubble Sort | Easy | [Link](problems/018_bubble_sort/) |
| 019 | Selection Sort | Easy | [Link](problems/019_selection_sort/) |
| 020 | Insertion Sort | Easy | [Link](problems/020_insertion_sort/) |
| 021 | Merge Sort | Medium | [Link](problems/021_merge_sort/) |
| 022 | Quick Sort | Medium | [Link](problems/022_quick_sort/) |
| 023 | Stack Implementation | Easy | [Link](problems/023_stack_implementation/) |
| 024 | Queue Implementation | Easy | [Link](problems/024_queue_implementation/) |
| 025 | Linked List Implementation | Medium | [Link](problems/025_linked_list_implementation/) |
| 026 | Reverse Linked List | Easy | [Link](problems/026_reverse_linked_list/) |
| 027 | Detect Cycle in Linked List | Medium | [Link](problems/027_detect_cycle_linked_list/) |
| 028 | Balanced Parentheses | Easy | [Link](problems/028_balanced_parentheses/) |
| 029 | Evaluate Postfix | Medium | [Link](problems/029_evaluate_postfix/) |
| 030 | Infix to Postfix | Medium | [Link](problems/030_infix_to_postfix/) |
| 031 | Decimal to Binary | Easy | [Link](problems/031_decimal_to_binary/) |
| 032 | Binary to Decimal | Easy | [Link](problems/032_binary_to_decimal/) |
| 033 | GCD | Easy | [Link](problems/033_gcd/) |
| 034 | LCM | Easy | [Link](problems/034_lcm/) |
| 035 | Power Function | Medium | [Link](problems/035_power_function/) |
| 036 | Square Root | Medium | [Link](problems/036_square_root/) |
| 037 | Armstrong Number | Easy | [Link](problems/037_armstrong_number/) |
| 038 | Perfect Number | Easy | [Link](problems/038_perfect_number/) |
| 039 | Strong Number | Easy | [Link](problems/039_strong_number/) |
| 040 | Happy Number | Easy | [Link](problems/040_happy_number/) |
| 041 | Count Words in String | Easy | [Link](problems/041_count_words/) |
| 042 | Capitalize First Letter | Easy | [Link](problems/042_capitalize_first_letter/) |
| 043 | Title Case | Easy | [Link](problems/043_title_case/) |
| 044 | Caesar Cipher | Easy | [Link](problems/044_caesar_cipher/) |
| 045 | Vigenère Cipher | Medium | [Link](problems/045_vigenere_cipher/) |
| 046 | Run-Length Encoding | Easy | [Link](problems/046_run_length_encoding/) |
| 047 | RLE Decoding | Easy | [Link](problems/047_rle_decoding/) |
| 048 | String Compression | Medium | [Link](problems/048_string_compression/) |
| 049 | String Rotation | Easy | [Link](problems/049_string_rotation/) |
| 050 | Longest Common Prefix | Easy | [Link](problems/050_longest_common_prefix/) |
| 051 | Longest Palindromic Substring | Medium | [Link](problems/051_longest_palindromic_substring/) |
| 052 | Longest Substring Without Repeating Chars | Medium | [Link](problems/052_longest_substring_no_repeat/) |
| 053 | String to Integer (atoi) | Medium | [Link](problems/053_string_to_integer/) |
| 054 | Implement strStr() | Easy | [Link](problems/054_implement_strstr/) |
| 055 | Valid Parentheses | Easy | [Link](problems/055_valid_parentheses/) |
| 056 | Merge Two Sorted Lists | Easy | [Link](problems/056_merge_two_sorted_lists/) |
| 057 | Remove Nth Node From End | Medium | [Link](problems/057_remove_nth_node_from_end/) |
| 058 | Add Two Numbers | Medium | [Link](problems/058_add_two_numbers/) |
| 059 | Swap Nodes in Pairs | Medium | [Link](problems/059_swap_nodes_in_pairs/) |
| 060 | Rotate Array | Medium | [Link](problems/060_rotate_array/) |
| 061 | Contains Duplicate | Easy | [Link](problems/061_contains_duplicate/) |
| 062 | Product of Array Except Self | Medium | [Link](problems/062_product_of_array_except_self/) |
| 063 | Maximum Subarray | Medium | [Link](problems/063_maximum_subarray/) |
| 064 | Maximum Product Subarray | Medium | [Link](problems/064_maximum_product_subarray/) |
| 065 | Find All Duplicates in Array | Medium | [Link](problems/065_find_all_duplicates/) |
| 066 | Move Zeroes | Easy | [Link](problems/066_move_zeroes/) |
| 067 | Two Sum II | Easy | [Link](problems/067_two_sum_ii/) |
| 068 | Three Sum | Medium | [Link](problems/068_three_sum/) |
| 069 | Four Sum | Medium | [Link](problems/069_four_sum/) |
| 070 | Container With Most Water | Medium | [Link](problems/070_container_with_most_water/) |
| 071 | Trapping Rain Water | Hard | [Link](problems/071_trapping_rain_water/) |
| 072 | Best Time to Buy and Sell Stock | Easy | [Link](problems/072_best_time_to_buy_and_sell_stock/) |
| 073 | Climbing Stairs | Easy | [Link](problems/073_climbing_stairs/) |
| 074 | Coin Change | Medium | [Link](problems/074_coin_change/) |
| 075 | Longest Increasing Subsequence | Medium | [Link](problems/075_longest_increasing_subsequence/) |
| 076 | Edit Distance | Hard | [Link](problems/076_edit_distance/) |
| 077 | 0/1 Knapsack | Medium | [Link](problems/077_01_knapsack/) |
| 078 | Unbounded Knapsack | Medium | [Link](problems/078_unbounded_knapsack/) |
| 079 | Subset Sum | Medium | [Link](problems/079_subset_sum/) |
| 080 | Partition Equal Subset Sum | Medium | [Link](problems/080_partition_equal_subset_sum/) |
| 081 | Word Break | Medium | [Link](problems/081_word_break/) |
| 082 | Matrix Chain Multiplication | Hard | [Link](problems/082_matrix_chain_multiplication/) |
| 083 | N-Queens | Hard | [Link](problems/083_n_queens/) |
| 084 | Sudoku Solver | Hard | [Link](problems/084_sudoku_solver/) |
| 085 | Rat in a Maze | Medium | [Link](problems/085_rat_in_a_maze/) |
| 086 | Knight's Tour | Hard | [Link](problems/086_knights_tour/) |
| 087 | Graph BFS | Easy | [Link](problems/087_graph_bfs/) |
| 088 | Graph DFS | Easy | [Link](problems/088_graph_dfs/) |
| 089 | Dijkstra's Algorithm | Medium | [Link](problems/089_dijkstra/) |
| 090 | Bellman-Ford | Medium | [Link](problems/090_bellman_ford/) |
| 091 | Floyd-Warshall | Medium | [Link](problems/091_floyd_warshall/) |
| 092 | Topological Sort | Medium | [Link](problems/092_topological_sort/) |
| 093 | Union-Find | Medium | [Link](problems/093_union_find/) |
| 094 | Kruskal's Algorithm | Medium | [Link](problems/094_kruskal/) |
| 095 | Prim's Algorithm | Medium | [Link](problems/095_prim/) |
| 096 | Trie Implementation | Medium | [Link](problems/096_trie/) |
| 097 | Heap Implementation | Medium | [Link](problems/097_heap/) |
| 098 | Priority Queue | Easy | [Link](problems/098_priority_queue/) |
| 099 | LRU Cache | Medium | [Link](problems/099_lru_cache/) |
| 100 | LFU Cache | Hard | [Link](problems/100_lfu_cache/) |

</details>

---

## 📌 Example Problem Walkthrough

### 001. Two Sum

**Problem:** Given an array of integers `nums` and an integer `target`, return indices of the two numbers that add up to `target`.

**File:** `problems/001_two_sum/solution.py`

```python
from typing import List


def two_sum(nums: List[int], target: int) -> List[int]:
    """
    Return indices of the two numbers such that they add up to target.

    Args:
        nums: List of integers.
        target: Target sum.

    Returns:
        A list with the two indices, or [] if no solution exists.
    """
    seen: dict[int, int] = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []
```

**Test:** `tests/test_001_two_sum.py`

```python
from problems.001_two_sum.solution import two_sum


def test_two_sum_basic():
    assert two_sum([2, 7, 11, 15], 9) == [0, 1]


def test_two_sum_no_solution():
    assert two_sum([1, 2, 3], 7) == []


def test_two_sum_negative_numbers():
    assert two_sum([-3, 4, 3, 90], 0) == [0, 2]


def test_two_sum_duplicates():
    assert two_sum([3, 3], 6) == [0, 1]
```

---

## 🛠 How to Add a New Problem

1. Create the folder: `problems/XXX_problem_name/`.
2. Add three files:
   - `README.md` — problem statement, examples, constraints.
   - `solution.py` — solution with type hints and docstrings.
   - `__init__.py` — empty file (makes it a package).
3. Add the test: `tests/test_XXX_problem_name.py`.
4. Update the **Problem Index** table above.
5. Run tests locally:
   ```bash
   pytest -v
   ```
6. Commit and push:
   ```bash
   git add .
   git commit -m "Add problem 101: <name>"
   git push
   ```

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. **Fork** the repository.
2. **Create a branch:**
   ```bash
   git checkout -b feature/add-problem-101
   ```
3. **Add your problem and tests.**
4. **Run the test suite:**
   ```bash
   pytest -v
   ```
5. **Commit your changes:**
   ```bash
   git commit -m "Add problem 101: <name>"
   ```
6. **Push and open a Pull Request.**

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.  
All PRs must pass CI before merging.

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

- **Author:** Your Name
- **Email:** your.email@example.com
- **GitHub:** [@your-username](https://github.com/your-username)
- **Project Link:** [https://github.com/your-username/100-python-problems](https://github.com/your-username/100-python-problems)

---

## 🙏 Acknowledgments

- Inspired by common coding interview questions and Python practice platforms.
- Thanks to all contributors who help improve this collection.
- Built with ❤️ for the Python community.

---

⭐ **If you find this project useful, please give it a star!** ⭐
