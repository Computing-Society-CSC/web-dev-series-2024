#### **Challenging Task 1: Understanding Functions**

- **Python**: Write a function that calculates the factorial of a number using recursion.
  ```python
  def factorial(n):
      if n == 1:
          return 1
      return n * factorial(n - 1)
  
  print(factorial(5))  # Output: 120
  ```

- **C++**: Write a function that calculates the nth Fibonacci number using recursion.
  ```cpp
  int fibonacci(int n) {
      if (n <= 1) return n;
      return fibonacci(n - 1) + fibonacci(n - 2);
  }
  
  cout << fibonacci(5);  // Output: 5
  ```

---

#### **Challenging Task 2: Working with Lists, Dictionaries, and Arrays**

- **Python (Dictionaries)**: Create a function that takes a dictionary of names and ages and returns the name of the oldest person.
  ```python
  def oldest_person(people):
      return max(people, key=people.get)
  
  ages = {"Alice": 25, "Bob": 30, "Charlie": 35}
  print(oldest_person(ages))  # Output: Charlie
  ```

- **C++ (Arrays)**: Write a function to search for a number in a sorted array using binary search (O(log n)).
  ```cpp
  int binary_search(int arr[], int size, int target) {
      int left = 0, right = size - 1;
      while (left <= right) {
          int mid = left + (right - left) / 2;
          if (arr[mid] == target)
              return mid;
          if (arr[mid] < target)
              left = mid + 1;
          else
              right = mid - 1;
      }
      return -1; // Element not found
  }
  
  int arr[] = {1, 2, 3, 4, 5};
  cout << binary_search(arr, 5, 3);  // Output: 2 (index of element 3)
  ```

---

#### **Challenging Task 3: Hands-On Practice**

##### **Bubble Sort Implementation**

- **Python**: Write a sorting program using bubble sort.
  ```python
  def bubble_sort(arr):
      n = len(arr)
      for i in range(n):
          for j in range(0, n-i-1):
              if arr[j] > arr[j+1]:
                  arr[j], arr[j+1] = arr[j+1], arr[j]
  
  arr = [64, 34, 25, 12, 22, 11, 90]
  bubble_sort(arr)
  print(arr)  # Output: [11, 12, 22, 25, 34, 64, 90]
  ```

- **C++**: Write a sorting program using bubble sort.
  ```cpp
  void bubble_sort(int arr[], int n) {
      for (int i = 0; i < n-1; i++) {
          for (int j = 0; j < n-i-1; j++) {
              if (arr[j] > arr[j+1]) {
                  int temp = arr[j];
                  arr[j] = arr[j+1];
                  arr[j+1] = temp;
              }
          }
      }
  }
  
  int arr[] = {64, 34, 25, 12, 22, 11, 90};
  int n = sizeof(arr)/sizeof(arr[0]);
  bubble_sort(arr, n);
  for (int i = 0; i < n; i++) {
      cout << arr[i] << " ";  // Output: 11 12 22 25 34 64 90
  }
  ```

---

##### **Fast Sort (Quicksort) Implementation**

- **Python**: Write a sorting program using quicksort.
  ```python
  def quicksort(arr):
      if len(arr) <= 1:
          return arr
      pivot = arr[len(arr) // 2]
      left = [x for x in arr if x < pivot]
      middle = [x for x in arr if x == pivot]
      right = [x for x in arr if x > pivot]
      return quicksort(left) + middle + quicksort(right)
  
  arr = [64, 34, 25, 12, 22, 11, 90]
  sorted_arr = quicksort(arr)
  print(sorted_arr)  # Output: [11, 12, 22, 25, 34, 64, 90]
  ```

- **C++**: Write a sorting program using quicksort.
  ```cpp
  void quicksort(vector<int>& nums, int left, int right) {
    if (left >= right) return;  // Base case: If there are one or no elements, it's already sorted.

    // Randomly choose a pivot and swap it with the left element
    int randomPivot = left + rand() % (right - left + 1);
    swap(nums[left], nums[randomPivot]);
    
    int pivot = nums[left];  // Store the pivot value
    int i = left + 1;
    int j = right;

    // Partition the array
    while (i <= j) {
        // Move 'i' right to find the first element greater than the pivot
        while (i <= j && nums[i] <= pivot) i++;
        // Move 'j' left to find the first element less than or equal to the pivot
        while (i <= j && nums[j] > pivot) j--;
        
        // Swap out-of-place elements
        if (i < j) {
            swap(nums[i], nums[j]);
        }
    }

    // Swap pivot into its correct position
    swap(nums[left], nums[j]);

    // Recursively sort the left and right partitions
    quicksort(nums, left, j - 1);
    quicksort(nums, j + 1, right);
}
  ```
