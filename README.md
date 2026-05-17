# Trie Data Structure in C++

![Language](https://img.shields.io/badge/Language-C++-blue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Data Structure](https://img.shields.io/badge/Type-Trie-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A complete implementation of the Trie (Prefix Tree) data structure in C++, supporting insertion, search, prefix checking, and autocomplete functionality.

---

## Features

* Insert words into the Trie
* Search for exact words
* Check if a prefix exists
* Autocomplete suggestions based on prefix
* Handles edge cases (empty input, case normalization)

---

## What is a Trie?

A Trie is a tree-like data structure used for efficient retrieval of strings.

### Key Properties

* Each node represents a character
* Paths represent words
* Lookup time is O(L), where L is the length of the word

---

## Implementation Details

### TrieNode

Each node contains:

* `children[26]` → pointers to child nodes
* `isEndOfWord` → marks complete words
* `storedWord` → stores the original word

### Trie Class Functions

| Function               | Description                           |
| ---------------------- | ------------------------------------- |
| `insert(word)`         | Inserts a word into the Trie          |
| `search(word)`         | Returns true if the word exists       |
| `startsWith(prefix)`   | Checks if any word starts with prefix |
| `autocomplete(prefix)` | Returns all matching words            |

---

## Example Usage

```cpp id="k9z1xq"
Trie trie;

trie.insert("apple");
trie.insert("application");

cout << trie.search("apple");        // true
cout << trie.startsWith("app");      // true

vector<string> results = trie.autocomplete("app");
// apple, application
```

---

## Test Coverage

The program includes:

* Basic insertion and search
* Prefix validation
* Autocomplete functionality
* Edge cases (empty string)
* Case sensitivity tests
* Additional dataset testing

---

## Notes

* Input is normalized using `tolower()`
* Only lowercase English letters (a-z) are supported
* Exact match depends on stored word comparison

---

## Project Structure

```id="p7m2sj"
├── main.cpp        # Trie implementation and tests
└── README.md       # Documentation
```

---

## Future Improvements

* Support uppercase and Unicode
* Word deletion
* Memory optimization
* Ranked autocomplete suggestions

---

## Complexity

| Operation    | Time Complexity |
| ------------ | --------------- |
| Insert       | O(L)            |
| Search       | O(L)            |
| Prefix       | O(L)            |
| Autocomplete | O(N * L)        |

---

## Author

Developed for data structures practice.

---

## Contribution

Contributions and improvements are welcome.
