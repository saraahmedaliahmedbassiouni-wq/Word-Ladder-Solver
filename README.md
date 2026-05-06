## Overview
This project is a **Word Ladder Solver** developed using Python.  
It finds the shortest transformation path between two words using the **Breadth-First Search (BFS)** algorithm. Each step changes only one letter, and all intermediate words must exist in a valid dictionary.

The project also includes a **Graphical User Interface (GUI)** built using Tkinter.

---

## Features

- Find shortest word transformation path
- Input validation and error handling
- Interactive GUI interface
- Step-by-step BFS-based search
- Reset and Help functionality
- Displays number of steps in the solution

---

## How the System Works

### Input
- Start word
- Target word  
(Both must be the same length and contain only letters)

---

### Process
The system uses **Breadth-First Search (BFS)**:
- Treats each word as a node in a graph
- Connects words that differ by exactly one letter
- Explores level by level to guarantee shortest path

---

### Output
- Displays transformation path (e.g., cat → cot → dot → dog)
- Shows number of steps
- Shows error messages when input is invalid

---

## Why BFS was Used

- Guarantees shortest transformation path
- Works perfectly for unweighted graph structure
- Efficient and avoids unnecessary exploration
- Simple queue-based implementation

---

## Libraries Used

- `nltk` – Word dictionary
- `collections.deque` – BFS queue
- `string` – Alphabet operations
- `tkinter` – GUI creation
- `messagebox` – Error and info popups

---

## Algorithm Explanation

### 1. Dictionary Loading
- Loads English words using NLTK corpus
- Downloads dataset if not available

---

### 2. Word Filtering
- Filters words based on required length

---

### 3. Neighbor Generation
- Generates all valid words differing by one letter
- Checks if word exists in dictionary

---

### 4. BFS Algorithm
- Starts from the initial word
- Explores all valid transformations
- Uses queue and visited set
- Returns shortest path if found

---

## GUI Features

### Main Window
- Title: Word Ladder Solver
- Size: 900x600
- Background: Light blue

---

### Components
- Input fields:
  - Start word
  - Target word

- Buttons:
  - Find Word Ladder (Run BFS)
  - Reset (Clear fields)
  - Help (Instructions popup)

- Output box:
  - Displays solution path

- Status bar:
  - Shows system messages

---

## Error Handling Cases

The system handles multiple input errors:

- Empty start or target word
- Only one field filled
- Words of different lengths
- Non-alphabetic characters
- Spaces inside words

Each case shows a clear error message to the user.

---

## Functions Overview

### Help Function
Displays instructions on how to use the system.

### Submit Function
- Validates input
- Runs BFS algorithm
- Displays result or error message

### Reset Function
- Clears all input and output fields

---

## How to Run

```bash id="run1"
python main.py
