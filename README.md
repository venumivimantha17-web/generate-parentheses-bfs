# Generate Parentheses Using BFS

A Python implementation of a **Breadth-First Search (BFS)** algorithm to generate all valid combinations of parentheses for a given number of pairs.

## 📌 Description

This project generates every possible valid combination of parentheses using a queue-based BFS approach.

For example, when the input is `3`, the program generates:

```text
((()))
(()())
(())()
()(())
()()()
```

The algorithm ensures that:

* The number of opening parentheses never exceeds the requested number of pairs.
* A closing parenthesis is only added when there are more opening parentheses than closing parentheses.
* Only complete and valid combinations are added to the result.

## Features

* Breadth-First Search (BFS) implementation
* Input type validation
* Input range validation
* Generates all valid parentheses combinations
* Uses a queue to track BFS states
* Simple and beginner-friendly Python implementation

## 🛠️ Technologies

* **Python 3**
* **Breadth-First Search (BFS)**
* **Queue Data Structure**

## 📂 Project Structure

```text
generate-parentheses-bfs/
│
├── generate_parentheses.py
└── README.md
```

## ▶️ How to Run

Make sure Python 3 is installed on your computer.

Run the program using:

```bash
python generate_parentheses.py
```

## Example

### Input

```python
gen_parentheses(3)
```

### Output

```text
['((()))', '(()())', '(())()', '()(())', '()()()']
```

## 🔍 Input Validation

The function checks whether the input is valid.

If the input is not an integer:

```python
gen_parentheses("3")
```

Output:

```text
The number of pairs should be an integer
```

If the number is less than `1`:

```python
gen_parentheses(0)
```

Output:

```text
The number of pairs should be at least 1
```

## How the BFS Algorithm Works

Each BFS state contains three values:

```text
(current_string, opening_parentheses_used, closing_parentheses_used)
```

The algorithm starts with:

```text
('', 0, 0)
```

At each step:

1. Add an opening parenthesis if fewer than `pairs` opening parentheses have been used.
2. Add a closing parenthesis only if it does not make the parentheses invalid.
3. Continue processing states using the queue.
4. When the current string reaches `2 × pairs` characters, add it to the result.

## ⏱️ Complexity

The number of valid combinations is the `n`th **Catalan number**, so the number of generated results grows rapidly as `n` increases.

The algorithm therefore requires exponential time and space relative to the number of pairs because it must generate and store all valid combinations.

## 🎯 Purpose

This project was created as a practical exercise in:

* Breadth-First Search
* Queue-based algorithms
* State management
* Input validation
* Python functions and data structures

## 📜 License

This project is available for educational and personal portfolio purposes.
