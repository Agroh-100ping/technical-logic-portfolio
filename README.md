# Technical Code Evaluation & Logic Portfolio

This repository showcases my ability to write clean, logical code in JavaScript and Python, analyze algorithmic efficiency, and write high-level technical critiques for code reviews.

---

## Module 1: JavaScript Execution & Edge Cases
### 1. Code Implementation (String Reversal & Cleansing)
```javascript
function cleanAndReverseString(str) {
    if (typeof str !== 'string') {
        throw new Error("Input must be a valid string");
    }
    // Removes non-alphanumeric characters, converts to lowercase, and reverses
    const cleanStr = str.replace(/[^a-zA-Z0-9]/g, '').toLowerCase();
    return cleanStr.split('').reverse().join('');
}
```
### 2. Technical Evaluation
* **Algorithmic Complexity:** The time complexity is **O(n)** where *n* is the length of the string, as `replace`, `split`, `reverse`, and `join` each traverse the array linearly. The space complexity is **O(n)** to store the newly generated string arrays.
* **Edge-Case Handling:** Safely handles empty strings `""`, inputs with only special characters, and rejects invalid data types (numbers, arrays) using strict type-checking logic.

---

## Module 2: Python Data Manipulation & Constraints
### 1. Code Implementation (Finding Duplicates)
```python
def find_unique_elements(input_list: list) -> list:
    if not isinstance(input_list, list):
        raise TypeError("Input must be a list data type")
        
    # Preserves order while filtering duplicates using a hash set
    seen = set()
    unique_list = []
    for item in input_list:
        if item not in seen:
            seen.add(item)
            unique_list.append(item)
    return unique_list
```
### 2. Technical Evaluation
* **Algorithmic Complexity:** Time complexity is optimized to **O(n)** because looking up elements and adding them to a Python `set` runs in **O(1)** average time. Space complexity is **O(n)** to maintain the hash set.
* **Logic Rationale:** Using a native hash set ensures optimal execution compared to a naive nested-loop approach, which would bottleneck at a slow **O(n²)** runtime.
