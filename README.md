# 100 Python Problems — Solutions & Tests

> A curated collection of 100 Python coding problems with clean solutions and comprehensive unit tests.  
> Perfect for practice, interview preparation, and learning Python.

[![Python](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/)
[![Tests](https://github.com/your-username/100-python-problems/actions/workflows/tests.yml/badge.svg)](https://github.com/your-username/100-python-problems/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📖 Table of Contents

- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Running Tests](#-running-tests)
- [Example Problem](#-example-problem)
- [Problem Index](#-problem-index)
- [How to Add a New Problem](#-how-to-add-a-new-problem)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

- **100 problems** covering basics, strings, lists, dictionaries, algorithms, data structures, and more.
- Each problem has its own folder with:
  - `README.md` — problem description and examples.
  - `solution.py` — clean, well-documented solution.
  - `__init__.py` — makes the folder a Python package.
- **Unit tests** for every solution using `pytest`.
- **Type hints** and **docstrings** for readability.
- Difficulty labels: **Easy**, **Medium**, **Hard**.
- GitHub Actions CI to run tests automatically.

---

## 📁 Project Structure

```text
100-python-problems/
├── problems/
│   ├── 001_two_sum/
│   │   ├── README.md
│   │   ├── solution.py
│   │   └── __init__.py
│   ├── 002_reverse_string/
│   │   ├── README.md
│   │   ├── solution.py
│   │   └── __init__.py
│   └── ...
├── tests/
│   ├── test_001_two_sum.py
│   ├── test_002_reverse_string.py
│   └── ...
├── .github/
│   └── workflows/
│       └── tests.yml
├── requirements.txt
├── pytest.ini
├── LICENSE
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- pip

### Installation

```bash
git clone https://github.com/your-username/100-python-problems.git
cd 100-python-problems

python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

pip install -r requirements.txt
```

---

## 💡 Usage

Run a solution directly:

```bash
python -m problems.001_two_sum.solution
```

Or import it in your own code:

```python
from problems.001_two_sum.solution import two_sum

result = two_sum([2, 7, 11, 15], 9)
print(result)  # [0, 1]
```

---

## 🧪 Running Tests

Run all tests:

```bash
pytest -v
```

Run a specific test file:

```bash
pytest tests/test_001_two_sum.py -v
```

Run tests with coverage:

```bash
pytest --cov=problems tests/
```

---

## 📌 Example Problem

### 001. Two Sum

**Problem:** Given an array of integers `nums` and an integer `target`, return indices of the two numbers that add up to `target`.

**Solution:** `problems/001_two_sum/solution.py`

```python
from typing import List


def two_sum(nums: List[int], target: int) -> List[int]:
    """
    Return indices of the two numbers such that they add up to target.

    Args:
        nums: List of integers.
        target: Target sum.

    Returns:
        A list containing the two indices, or an empty list if no solution exists.
    """
    seen = {}
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
| 052 | Longest Substring Without Repeating Characters | Medium | [Link](problems/052_longest_substring_no_repeat/) |
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

## 🛠 How to Add a New Problem

1. Create a new folder under `problems/` using the format `XXX_problem_name/`.
2. Add:
   - `README.md` — problem statement, examples, constraints.
   - `solution.py` — your solution with type hints and docstrings.
   - `__init__.py` — empty file to make it a package.
3. Add a test file under `tests/` named `test_XXX_problem_name.py`.
4. Update the **Problem Index** table in this README.
5. Run the tests:
   ```bash
   pytest -v
   ```

---

## 🤝 Contributing

Contributions are welcome! Here’s how you can help:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/add-problem-101
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add problem 101: Example Problem"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/add-problem-101
   ```
5. Open a Pull Request.

Please make sure all tests pass before submitting a PR.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Inspired by common coding interview questions and Python practice platforms.
- Thanks to all contributors who help improve this collection.

---

⭐ If you find this project useful, please consider giving it a star!
