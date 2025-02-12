## 📝 **Cheat Sheet: Answers to the Challenges**

### **Challenge 1: Design a Data Structure for a Competition**

#### **Python:**
```python
# Creating a dictionary to store competition information
competition = {
    "Team A": [("John", 10), ("Jane", 12)],
    "Team B": [("Mike", 8), ("Lucy", 15)]
}

# Accessing and displaying team data
team_name = "Team A"
team_info = competition[team_name]
for member, score in team_info:
    print(f"{member} scored {score}")
```

#### **C++:**
```cpp
#include <iostream>
#include <map>
#include <vector>
using namespace std;

// Defining a struct for team members
struct TeamMember {
    string name;
    int score;
};

// Creating a map to store competition information
map<string, vector<TeamMember>> competition;

int main() {
    competition["Team A"] = {{"John", 10}, {"Jane", 12}};
    competition["Team B"] = {{"Mike", 8}, {"Lucy", 15}};

    // Accessing and displaying team data
    for (auto& team : competition) {
        cout << "Team: " << team.first << endl;
        for (auto& member : team.second) {
            cout << member.name << " scored " << member.score << endl;
        }
    }
}
```

---

### **Challenge 2: XOR with `and`, `or`, and `not`**

#### **Python:**
```python
# Function to perform XOR using only and, or, and not
def xor(a, b):
    return (a and not b) or (not a and b)

# Testing the XOR function
print(xor(True, False))  # Output: True
print(xor(True, True))   # Output: False
print(xor(False, False)) # Output: False
```

#### **C++:**
```cpp
#include <iostream>
using namespace std;

// Function to perform XOR using only and, or, and not
bool xor_op(bool a, bool b) {
    return (a && !b) || (!a && b);
}

int main() {
    // Testing the XOR function
    cout << xor_op(true, false) << endl;  // Output: 1 (True)
    cout << xor_op(true, true) << endl;   // Output: 0 (False)
    cout << xor_op(false, false) << endl; // Output: 0 (False)
}
```

---

### **Challenge 3: Check for Duplicate Characters in O(n)**

#### **Python (O(n) with two loops)**:
```python
# Checking for duplicate characters using two loops
word = "programming"
for i in range(len(word)):
    for j in range(i + 1, len(word)):
        if word[i] == word[j]:
            print(f"{word[i]} is repeated")
            break
```

#### **C++ (O(n) with two loops)**:
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string word = "programming";

    // Checking for duplicate characters using two loops
    for (int i = 0; i < word.length(); i++) {
        for (int j = i + 1; j < word.length(); j++) {
            if (word[i] == word[j]) {
                cout << word[i] << " is repeated" << endl;
                break;
            }
        }
    }
}
```

---

### **Challenge 4: Check for Duplicate Characters in O(n) Using Bit Manipulation (数位压缩)**

#### **Python (Using Bitwise Operations, O(n)):**
```python
# Using bit manipulation to check for duplicate characters
def find_duplicate_bitwise(word):
    checker = 0
    for char in word:
        val = ord(char) - ord('a')  # Adjust the range to handle lowercase letters
        if (checker & (1 << val)) > 0:
            print(f"{char} is repeated")
            return
        checker |= (1 << val)

# Test the function
find_duplicate_bitwise("programming")
```

#### **C++ (Using Bitwise Operations, O(n)):**
```cpp
#include <iostream>
#include <string>
using namespace std;

// Using bit manipulation to check for duplicate characters
void find_duplicate_bitwise(string word) {
    int checker = 0;
    for (char ch : word) {
        int val = ch - 'a';  // Adjusting for lowercase letters
        if ((checker & (1 << val)) > 0) {
            cout << ch << " is repeated" << endl;
            return;
        }
        checker |= (1 << val);
    }
}

int main() {
    // Test the function
    find_duplicate_bitwise("programming");
}
```
