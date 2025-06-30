<div align="center">
  <img src="./assets/CPP STL.png" alt="API Logo"/>
</div>

<h1 align="center">CPP STL DSA Reference</h1>

> [!TIP]
>
> This is not full reference for CPP STL, this doc only contains those CPP STL which are used frequently and important for DSA


## :card_index_dividers: Content

<details close>
<summary> 0. Getting Started </summary>

<h3 align="center"> ⚡ 0. Getting Started </h3>

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```
</details>
<details close>
<summary> 1. Vector </summary>

<h3 align="center"> ⚡ 1. Vector </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // ========== Declaration ========== //
    // Creates an empty vector of integers.
    vector<int> v;
    // Creates an empty vector of string.
    vector<string> vs;
    // Creates a vector of size 5, all elements initialized to 20.
    vector<int> v(5, 20);
    // Initializes with the given values.
    vector<int> v = {1, 2, 3, 4, 5};
    // Copies all elements from v1 to v2.
    vector<int> v1 = {1, 2, 3};
    vector<int> v2(v1);

    // 2D vector for matrices
    vector<vector<int>> mat;
    // ======================================== //
    // ======================================== //

    // ========== Adding Elements ========== //
    // Adds 13 to the end of the vector.
    v.push_back(13);
    v.emplace_back(13); // generally faster than <push_back>

    // Add 14 to the position (start) of the vector
    v.insert(v.begin(), 10);
    // ======================================== //
    // ======================================== //

    // ========== Deleting Elements ========== //
    // Delete element from end.
    v.pop_back();
    // Clear the whole vector.
    v.clear();
    // Erases element at position 1.
    v.erase(v.begin() + 1);
    // Erases first 2 element from start.
    v.erase(v.begin(), v.begin() + 2);
    // ======================================== //
    // ======================================== //

    // ========== Getting Elements ========== //
    // Using []
    v[0];
    // Using at()
    v.at(0);
    // Returns first element value
    v.front();
    // Returns last element value
    v.back();

    // Points to the first element (1)
    vector<int> vec = {1, 2, 3};
    auto it = vec.begin();
    // Points to the last element (1)
    vector<int> vec = {1, 2, 3};
    auto it = vec.end();

    // ======================================== //
    // ======================================== //

    // ========== Other Important Methods ========== //
    // Returns the number of elements in the vector.
    v.size();
    // Checks if the vector is empty
    v.empty(); // return true or false

    // Sorting [Time complexity: O(n log n)]
    sort(vec.begin(), vec.end());

    // Iterating vectors
    // you can use <int> instead of <auto>
    for (auto num : v)
    {
        cout << num << endl;
    }

    // Swapping two vectors
    vector<int> vec1 = {1, 2, 3};
    vector<int> vec2 = {4, 5, 6};
    vec1.swap(vec2); // vec1 = {4, 5, 6}, vec2 = {1, 2, 3}

    // ======================================== //
    // ======================================== //
    return 0;
}

```
</details>
<details close>
<summary> 2. Stack </summary>

<h3 align="center"> ⚡ 2. Stack </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // ========== Declaration ========== //
    // Creates an empty stack of integers.
    stack<int> st;
    // Creates an empty stack of strings.
    stack<string> st_str;
    // ======================================== //

    // ========== Adding Elements ========== //
    // Adds 23 to the top of the stack.
    st.push(23);
    // Adds 34 to the top of the stack (alternative to push()).
    st.emplace(34);
    // Emplace is slightly more efficient as it constructs the element in-place.
    // ======================================== //

    // ========== Deleting Elements ========== //
    // Removes the top element from the stack.
    st.pop();
    // ======================================== //

    // ========== Accessing Elements ========== //
    // Returns the top element of the stack.
    int top_element = st.top();
    // ======================================== //

    // ========== Other Important Methods ========== //
    // Checks if the stack is empty.
    st.empty(); // Returns true or false.
    // Returns the number of elements in the stack.
    st.size();

    // Swapping two stacks.
    stack<int> st2;
    st2.swap(st); // Swaps the elements of st and st2.
    // ======================================== //

    // ========== Iterating Through Stack ========== //
    // Iterates through the stack and prints elements.
    // Note: Direct indexing is not allowed in stacks.
    while (!st.empty())
    {
        // Prints the top element of the stack.
        std::cout << st.top() << std::endl;
        // Removes the top element from the stack.
        st.pop();
    }
    // ======================================== //

    return 0;
}
```
</details>
<details close>
<summary> 3. Queue </summary>

<h3 align="center"> ⚡ 3. Queue </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // ========== Working Principal ========== //
    // FIFO --> First In First Out
    // ======================================== //
    // ======================================== //

    // ========== Declaration ========== //
    // Creates an empty queue of integers.
    queue<int> que;
    // Creates an empty queue of strings.
    queue<string> que_str;
    // ======================================== //
    // ======================================== //

    // ========== Adding Elements ========== //
    // Adds 1 at the end of the queue.
    que.push(1);
    que.push(2);
    // (alternative to push()).
    que.emplace(3); // generally faster than <push>
    // ======================================== //
    // ======================================== //

    // ========== Deleting Elements ========== //
    // Removes the front element from the queue.
    que.pop();
    // Clear the whole queue.
    while (!que.empty())
    {
        que.pop();
    }
    // ======================================== //
    // ======================================== //

    // ========== Accessing Elements ========== //
    // Returns the front element of the queue.
    int front_element = que.front();
    // Returns the back/end element of the queue.
    int back_element = que.back();
    // ======================================== //
    // ======================================== //

    // ========== Other Important Methods ========== //
    // Checks if the queue is empty.
    que.empty(); // Returns true or false.
    // Returns the number of elements in the queue.
    que.size();

    // Copying the queue to another queue
    queue<int> tmp_que = que;

    // Swapping two queues.
    queue<int> que2;
    que2.swap(que); // Swaps the elements of que and que2.
    // ======================================== //
    // ======================================== //

    // ========== Iterating Through Queue ========== //
    // Iterates through the queue and prints elements.
    // Note: Direct indexing is not allowed in queues.
    while (!que.empty())
    {
        // Prints the front element of the queue.
        std::cout << que.front() << std::endl;
        // Removes the front element from the queue.
        que.pop();
    }

    // RECOMMENDED METHOD FOR INTERATING:
    std::queue<int> temp = que; // Copy the original queue
    // so that original queue remain same, for future reference
    // but to <reduce time complexity> you can use above method :)
    while (!temp.empty())
    {
        std::cout << temp.front() << " ";
        temp.pop();
    }
    // ======================================== //
    // ======================================== //

    return 0;
}
```
</details>
<details close>
<summary> 4. Priority-Queue </summary>

<h3 align="center"> ⚡ 4. Priority-Queue </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // ========== Working Principle ========== //
    // Max-Heap by default: Largest element at the top
    // ======================================== //
    // ======================================== //

    // ========== Declaration ========== //
    // Max-Heap (default)
    priority_queue<int> max_pq;

    // Min-Heap
    priority_queue<int, vector<int>, greater<int>> min_pq;

    // Max-Heap for strings (lexicographical)
    priority_queue<string> str_pq;
    // ======================================== //
    // ======================================== //

    // ========== Adding Elements ========== //
    max_pq.push(10);
    max_pq.push(30);
    max_pq.emplace(20); // Generally faster than push
    // ======================================== //
    // ======================================== //

    // ========== Deleting Elements ========== //
    // Removes the top (largest) element.
    max_pq.pop();
    // Clear the entire priority_queue.
    while (!max_pq.empty())
    {
        max_pq.pop();
    }
    // ======================================== //
    // ======================================== //

    // ========== Accessing Elements ========== //
    // Returns the top element (max for max-heap, min for min-heap).
    int top_element = max_pq.top();
    // ======================================== //
    // ======================================== //

    // ========== Other Important Methods ========== //
    // Check if the priority_queue is empty.
    max_pq.empty(); // Returns true or false.
    // Returns the number of elements in the queue.
    max_pq.size();

    // Copying to another priority_queue
    priority_queue<int> temp_pq = max_pq;

    // Swapping two priority_queues
    priority_queue<int> another_pq;
    another_pq.swap(max_pq);
    // ======================================== //
    // ======================================== //

    // ========== Iterating Through Priority Queue ========== //
    // NOTE: No direct indexing
    // So we copy and iterate

    std::priority_queue<int> pq_copy = max_pq;
    while (!pq_copy.empty())
    {
        std::cout << pq_copy.top() << " ";
        pq_copy.pop();
    }
    std::cout << std::endl;

    // For min-heap
    min_pq.push(5);
    min_pq.push(1);
    min_pq.push(3);

    std::priority_queue<int, vector<int>, greater<int>> min_copy = min_pq;
    while (!min_copy.empty())
    {
        std::cout << min_copy.top() << " ";
        min_copy.pop();
    }
    std::cout << std::endl;

    // ======================================== //
    // ======================================== //

    return 0;
}
```
</details>
<details close>
<summary> 5. Set </summary>

<h3 align="center"> ⚡ 5. Set </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{

    // ========== Note ========== //
    // std::set is always sorted in ascending order by default.

    // ========== Declaration ========== //
    // Creates an empty set of integers.
    set<int> s;
    // Creates an empty set of string.
    set<string> s;
    // Creates a set containing {5, 20, 60}.
    set<int> s{5, 20, 60};
    // Creates a set containing {5, 20, 60}.
    set<int> s = {5, 20, 60};
    // ======================================== //
    // ======================================== //

    // ========== Adding New Elements ========== //
    // Adds 13 to the set.
    s.insert(13);
    s.emplace(14);
    // For int, insert() and emplace() are effectively the same.

    // emplace_hint will insert 20 after 10
    auto it = s.find(10);
    s.emplace_hint(it, 20); // Hint: insert near 10
    // ======================================== //
    // ======================================== //

    // ========== Deleting Elements ========== //
    // Delete element from the set.
    s.erase(10);
    
    // Removes all elements.
    s.clear();

    // Erases element by range
    // {10, 20, 30, 40, 50}
    auto start = s.find(20);
    auto end = s.find(50);
    s.erase(start, end); // removes 20, 30, 40
    // ======================================== //
    // ======================================== //

    // ========== Accessing Elements ========== //
    // find(value)	Returns iterator to element or end() if not found.
    auto it = s.find(20);
    if (it != s.end())
        std::cout << "Found: " << *it << "\n";
    else
        std::cout << "Not found\n";

    // count(value)	Returns 0 or 1 (since set stores unique elements).
    std::cout << "Count of 2: " << s.count(2) << "\n";

    // contains(value)	Returns true if value exists
    // #### (C++20+).
    // if (s.contains(200))
    //     std::cout << "Set contains 200\n";

    // Points to the first element in the set
    // begin() gives an iterator to the smallest element.
    if (!s.empty())
        std::cout << "First element: " << *s.begin() << "\n";

    // rbegin() start reverse of begin() ==> return last element (largest one as set is sorted by default)
    if (!s.empty())
        std::cout << "First element: " << *s.rbegin() << "\n";

    // ======================================== //
    // ======================================== //

    // ========== Other Important Methods ========== //
    // Returns the number of elements in the set.
    s.size();

    // Checks if the set is empty
    s.empty(); // return true or false

    // Iterating set
    // you can use <int> instead of <auto>
    // 🌸 Method 1:
    for (auto num : s)
        cout << num << endl;

    // Method 2:
    for (auto it = s.begin(); it != s.end(); it++)
        cout << *it << endl;

    // Swapping two sets
    set<int> set2 = {4, 5, 6};
    set<int> set1 = {1, 2, 3};
    set1.swap(set2); // set1 = {4, 5, 6}, set2 = {1, 2, 3}

    // ======================================== //
    // ======================================== //
    return 0;
}

```
</details>
<details close>
<summary> 6. Unordered-Set </summary>

<h3 align="center"> ⚡ 6. Unordered-Set </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{

    // ========== Note ========== //
    // std::unordered_set is not sorted, elements have no fixed order

    // ========== Declaration ========== //
    // Creates an empty unordered_set of integers.
    unordered_set<int> s;
    // Creates an empty unordered_set of string.
    unordered_set<string> s;
    // Creates a unordered_set containing {5, 20, 60}.
    unordered_set<int> s{5, 20, 60};
    // Creates a unordered_set containing {5, 20, 60}.
    unordered_set<int> s = {5, 20, 60};
    // ======================================== //
    // ======================================== //

    // ========== Adding New Elements ========== //
    // Adds 13 to the unordered_set;.
    s.insert(13);
    s.emplace(14);
    // For int, insert() and emplace() are effectively the same.

    // emplace_hint will insert 20 after 10
    // auto it = s.find(10);
    // s.emplace_hint(it, 20);
    // No emplace_hint() in unordered_set

    // ======================================== //
    // ======================================== //

    // ========== Deleting Elements ========== //
    // Delete element from the unordered_set.
    s.erase(10);

    // Removes all elements.
    s.clear();

    // Erases element by range
    // {10, 20, 30, 40, 50}
    auto start = s.find(20);
    auto end = s.find(50);
    s.erase(start, end); // removes 20, 30, 40
    // Order is undefined, but range erase still works based on iterators.

    // ======================================== //
    // ======================================== //

    // ========== Accessing Elements ========== //
    // find(value)	Returns iterator to element or end() if not found.
    auto it = s.find(20);
    if (it != s.end())
        std::cout << "Found: " << *it << "\n";
    else
        std::cout << "Not found\n";

    // count(value)	Returns 0 or 1 (since unordered_set  stores unique elements).
    std::cout << "Count of 2: " << s.count(2) << "\n";

    // contains(value)	Returns true if value exists
    // #### (C++20+).
    // if (s.contains(200))
    //     std::cout << "Unordered Set contains 200\n";

    // Points to the first element in the case of set
    // but for unordered_set
    // begin() not gives "first" in any order (asc or desc)
    if (!s.empty())
        std::cout << "Some element: " << *s.begin() << "\n";

    // ======================================== //
    // ======================================== //

    // ========== Other Important Methods ========== //
    // Returns the number of elements in the unordered_set.
    s.size();

    // Checks if the unordered_set is empty
    s.empty(); // return true or false

    // Iterating unordered_set
    // you can use <int> instead of <auto>
    // 🌸 Method 1:
    for (auto num : s)
        cout << num << endl;

    // Method 2:
    for (auto it = s.begin(); it != s.end(); it++)
        cout << *it << endl;

    // Swapping two unordered_sets
    unordered_set<int> set1 = {1, 2, 3};
    unordered_set<int> set2 = {4, 5, 6};
    set1.swap(set2); // set1 = {4, 5, 6}, set2 = {1, 2, 3}

    // ======================================== //
    // ======================================== //
    return 0;
}

```
</details>
<details close>
<summary> 7. Map </summary>

<h3 align="center"> ⚡ 7. Map </h3>

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // ========== Note ========== //
    // std::map stores key-value pairs
    // Keys are unique and sorted in ascending order by default
    // ======================================== //

    // ========== Declaration ========== //

    // Empty map of int to string
    // map<key, value> m;
    map<int, int> my_map;
    map<int, string> m;

    // Map initialized with key-value pairs
    map<int, string> m1 = {
        {1, "apple"},
        {2, "banana"},
        {3, "cherry"}};

    // Copy constructor
    map<int, string> m2 = m1;

    // ======================================== //
    // ======================================== //

    // ========== Adding New Elements ========== //

    // Method 1: insert() — using pair
    m.insert({4, "date"});

    // Method 2: emplace() — constructs in-place
    m.emplace(5, "elderberry");

    // Method 3: operator[] — inserts or updates
    // If key exists, then update it otherwise, insert it
    m[6] = "fig";       // inserts new pair
    m[2] = "blueberry"; // updates value for key 2

    // ======================================== //
    // ======================================== //

    // ========== Deleting Elements ========== //

    // Erase by key
    m.erase(4); // removes key 4

    // Removes all key-value pairs
    m.clear();

    // Erase by iterator
    auto it = m.find(3);
    if (it != m.end())
        m.erase(it); // removes key 3

    // Erase range
    auto start = m.begin();
    auto end = m.find(5); // not included
    m.erase(start, end);  // removes keys before 5
    // ======================================== //
    // ======================================== //

    // ========== Accessing Elements ========== //

    // Access using key (inserts default value if key is absent!)
    cout << m[1] << "\n"; // returns "" if key 1 not present

    // at operator
    cout << m.at(5) << "\n";

    // find() — returns iterator to key, or end() if not found
    if (m.find(2) != m.end())
        cout << "Found key 2\n";

    // count() — returns 1 if key exists, 0 otherwise
    cout << "Count of 6: " << m.count(6) << "\n";

    // ======================================== //
    // ======================================== //

    // ========== Iterating over map ========== //

    // 🌸 Method 1: range-based for loop
    for (auto [key, value] : m)
        cout << key << " => " << value << "\n";

    // Method 2: iterator
    for (auto it = m.begin(); it != m.end(); ++it)
        cout << it->first << " -> " << it->second << "\n";

    // ======================================== //
    // ======================================== //

    // ========== Other Useful Methods ========== //

    // Check if empty
    if (m.empty())
        cout << "Map is empty\n";

    // Size of map
    cout << "Map size: " << m.size() << "\n";

    // Swap with another map
    map<int, string> m3 = {{10, "grape"}, {20, "kiwi"}};
    map<int, string> m4 = {{1, "apple"}, {2, "banana"}};
    m3.swap(m4);

    // ======================================== //
    // ======================================== //

    return 0;
}

```
</details>
<details close>
<summary> 8. Unordered-Map </summary>

<h3 align="center"> ⚡ 8. Unordered-Map </h3>

```cpp
// Development in progress 🫣
```
</details>
<details close>
<summary> 9. Deque </summary>

<h3 align="center"> ⚡ 9. Deque </h3>

```cpp
// Development in progress 🫣
```
</details>
<details close>
<summary> 10. Pair </summary>

<h3 align="center"> ⚡ 10. Pair </h3>

```cpp
// Development in progress 🫣
```
</details>
<details close>
<summary> 11. List </summary>

<h3 align="center"> ⚡ 11. List </h3>

```cpp
// Development in progress 🫣
```
</details>


<!-- ## :memo: Todo -->
## :seedling: Todo

- [ ] ~~Getting started with cpp [will be added later]~~
- [x] Vector
- [x] Stack
- [x] Queue
- [x] Priority-Queue
- [x] Set
- [x] Unordered-Set
- [x] Map
- [ ] Unordered-Map
- [ ] List
- [ ] Deque
- [ ] Pair

> [!WARNING]
>
> The order may vary, and I will add some other STL components in the future.

## :hugs: Contributing
kindly refer to [CONTRIBUTING.md](./CONTRIBUTING.md)

## :compass: About
This project was created to serve as a quick reference for C++ STL while solving DSA problems. Over time, you may no longer need it.

![Status](https://img.shields.io/badge/Status%20-In%20Development%20-FFD700?style=for-the-badge)

![About Author](https://img.shields.io/badge/Created%20by-%20Saket%20Maurya-f5a97f?style=for-the-badge)

## :label: Attribution

C++ STL Poster created by - [artinwve](https://www.instagram.com/artinwve/)