# Fix My Code Challenge - Part 0 🐛

Welcome to the first set of debugging challenges! This directory contains basic debugging exercises across multiple programming languages to help you develop fundamental debugging skills.

## 📁 Challenge Files

```
0x00-challenge/
├── 0-fizzbuzz.py           # Python: FizzBuzz implementation
├── 1-print_square.js       # JavaScript: Square printing
├── 2-sort.rb              # Ruby: Integer sorting algorithm
├── 3-user.py              # Python: User class with password validation
├── 4-delete_dnodeint/     # C: Doubly linked list operations
│   ├── lists.h            # Header file with structure definitions
│   ├── main.c             # Test file for the functions
│   ├── print_dlistint.c   # Function to print doubly linked list
│   ├── add_dnodeint_end.c # Function to add node at end
│   ├── delete_dnodeint_at_index.c # Function to delete node (TO FIX)
│   └── free_dlistint.c    # Function to free memory
└── README.md              # This file
```

## 🎯 Learning Objectives

By the end of these challenges, you should be able to:
- Identify syntax errors in different programming languages
- Debug logical errors in algorithms
- Fix implementation issues in data structures
- Understand common programming mistakes
- Apply debugging techniques systematically

## 📝 Challenge Descriptions

### 0. FizzBuzz (Python)
**File**: `0-fizzbuzz.py`
**Language**: Python 3
**Issue**: Classic FizzBuzz implementation with potential bugs
**Skills**: Conditional logic, string manipulation, modular arithmetic

**Expected Output**:
```bash
./0-fizzbuzz.py 15
1 2 Fizz 4 Buzz Fizz 7 8 Fizz Buzz 11 Fizz 13 14 FizzBuzz
```

### 1. Print Square (JavaScript)
**File**: `1-print_square.js`
**Language**: Node.js
**Issue**: Square printing with character '#'
**Skills**: Nested loops, output formatting, command-line arguments

**Expected Output**:
```bash
./1-print_square.js 4
####
####
####
####
```

### 2. Sort Integers (Ruby)
**File**: `2-sort.rb`
**Language**: Ruby
**Issue**: Sorting algorithm for command-line integer arguments
**Skills**: Array manipulation, sorting algorithms, input validation

**Expected Output**:
```bash
ruby 2-sort.rb 12 41 2 C 9 -9 31 fun -1 32
-9 -1 2 9 12 31 32 41
```

### 3. User Class (Python)
**File**: `3-user.py`
**Language**: Python 3
**Issue**: User class with password hashing and validation
**Skills**: OOP, property decorators, MD5 hashing, input validation

**Expected Behavior**:
```python
u = User()
u.password = "my_password"
print(u.is_valid_password("my_password"))  # Should return True
print(u.is_valid_password("wrong"))        # Should return False
```

### 4. Delete Node (C)
**Directory**: `4-delete_dnodeint/`
**Language**: C
**Issue**: Doubly linked list node deletion function
**Skills**: Pointer manipulation, memory management, linked list operations

**Function to Fix**: `delete_dnodeint_at_index`
```c
int delete_dnodeint_at_index(dlistint_t **head, unsigned int index);
```

## 🚀 Getting Started

### Prerequisites
- **Python 3.x** (for Python challenges)
- **Node.js** (for JavaScript challenges)
- **Ruby** (for Ruby challenges)
- **GCC compiler** (for C challenges)

### Running the Challenges

1. **Python Files**:
   ```bash
   chmod +x 0-fizzbuzz.py
   ./0-fizzbuzz.py 15
   
   python3 3-user.py
   ```

2. **JavaScript Files**:
   ```bash
   chmod +x 1-print_square.js
   ./1-print_square.js 8
   ```

3. **Ruby Files**:
   ```bash
   ruby 2-sort.rb 12 41 2 9 -1
   ```

4. **C Files**:
   ```bash
   cd 4-delete_dnodeint/
   gcc -Wall -pedantic -Werror -Wextra *.c -o delete_dnodeint
   ./delete_dnodeint
   ```

## 🔍 Debugging Tips

1. **Read Error Messages Carefully**: They often point directly to the issue
2. **Understand the Expected Behavior**: Know what the code should do
3. **Use Print Debugging**: Add print statements to trace execution
4. **Check Edge Cases**: Test with boundary values
5. **Review Language Syntax**: Ensure proper syntax for each language

## ✅ Testing Your Solutions

Each challenge should:
- Compile/run without errors
- Produce expected output for given inputs
- Handle edge cases appropriately
- Follow language best practices

## 🎓 Skills Assessment

After completing these challenges, you should be comfortable with:
- [ ] Python syntax and error handling
- [ ] JavaScript/Node.js basics
- [ ] Ruby programming fundamentals
- [ ] C pointers and memory management
- [ ] Basic algorithm debugging
- [ ] Multi-language development environment

## 📚 Common Issues to Look For

- **Syntax Errors**: Missing semicolons, incorrect indentation
- **Logic Errors**: Wrong conditional statements, incorrect loops
- **Type Errors**: Incorrect data type handling
- **Memory Issues**: In C, watch for memory leaks and segmentation faults
- **Edge Cases**: Empty inputs, negative numbers, null pointers

## 📊 Progress Tracker

- [ ] 0-fizzbuzz.py - Fixed and tested
- [ ] 1-print_square.js - Fixed and tested  
- [ ] 2-sort.rb - Fixed and tested
- [ ] 3-user.py - Fixed and tested
- [ ] 4-delete_dnodeint/ - All functions working correctly

## 🔗 Next Steps

Once you complete this challenge set:
1. Move on to [0x01-challenge](../0x01-challenge/) for advanced debugging
2. Practice with additional coding problems
3. Learn advanced debugging tools for each language

---

**Remember**: The goal is not just to fix the code, but to understand why it was broken and how to prevent similar issues in the future! 🎯
