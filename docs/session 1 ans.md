## First Challenge

### Python

In Python, you can use triple quotes to create a multi-line string and print it:

```python
# basic version
print(" |\\__/,|   (`\\")
print(" |_ _  |.--.) )")
print(" ( T   )     /")
print("(((^_(((/(((_/")

# optional
ascii_art = """
 |\__/,|   (`\
 |_ _  |.--.) )
 ( T   )     /
(((^_(((/(((_/
"""

print(ascii_art)
```

Save this code in a file with a `.py` extension (e.g., `ascii_art.py`) and run it with Python to see the ASCII art printed on the screen.

### C++

In C++, you can use the `cout` stream to output multi-line strings:

```cpp
#include <iostream>
using namespace std;

int main() {
	# standard
    cout << " |\\__/,|   (`\\" << endl;
    cout << " |_ _  |.--.) )" << endl;
    cout << " ( T   )     /" << endl;
    cout << "(((^_(((/(((_/" << endl;

	# optional
	cout << R"(
	 |\__/,|   (`\
	 |_ _  |.--.) )
	 ( T   )     /
	(((^_(((/(((_/)";

    return 0;
}

```

---
