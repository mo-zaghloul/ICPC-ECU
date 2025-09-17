# STL (Standard Template Library) Notes II

## Pair
- Stores two values (can be of different types).
- Access elements using `.first` and `.second`.
- Often used in maps, sorting, and returning multiple values.

Example:
```cpp
pair<int, string> p = {1, "Alice"};
cout << p.first << " " << p.second;
```

---

## Set
- Stores **unique elements** in sorted order.
- Implemented as a balanced BST (usually Red-Black Tree).
- No random access (like arrays/vectors).
- Search, Insert, Erase → **O(log n)**.

**Common Operations:**
- `insert(x)`
- `erase(x)`
- `find(x)`
- `count(x)` → returns 0 or 1
- `begin()`, `end()`

---

## Multiset
- Stores elements in sorted order **but allows duplicates**.
- Same complexity as `set`.

**Common Operations:**
- `insert(x)`
- `erase(x)` → erases all occurrences of `x`
- `erase(s.find(x))` → erases only one occurrence
- `count(x)` → number of times `x` exists
- `find(x)`

---

## Map
- Stores **key-value pairs** with **unique keys**.
- Keys are sorted automatically.
- Implemented as balanced BST.
- Search, Insert, Erase → **O(log n)**.

**Common Operations:**
- `insert({key, value})`
- `m[key] = value` (insert or update)
- `erase(key)`
- `find(key)`
- `count(key)` → 0 or 1

Example:
```cpp
map<int, string> m;
m[1] = "Alice";
m[2] = "Bob";
for (auto &x : m)
    cout << x.first << " " << x.second << endl;
```

---

## Multimap
- Stores key-value pairs but allows **duplicate keys**.
- Keys remain sorted.
- Search, Insert, Erase → **O(log n)**.

**Common Operations:**
- `insert({key, value})`
- `erase(key)` → erases all pairs with this key
- `find(key)` → returns iterator to first occurrence
- `count(key)` → number of pairs with this key
- `equal_range(key)` → returns range of all pairs with this key

Example:
```cpp
multimap<int, string> mm;
mm.insert({1, "Alice"});
mm.insert({1, "Bob"});
for (auto &x : mm)
    cout << x.first << " " << x.second << endl;
```

---

## Priority Queue
- A container adapter that provides constant time access to the **largest element** (by default).
- Implemented using a **max-heap** (by default).
- By default, `priority_queue` is a **max-heap**. To make it a **min-heap**, use `greater<T>`.

**Common Operations:**
- `push(x)` → O(log n)
- `pop()` → O(log n)
- `top()` → O(1)
- `empty()`, `size()`

**Example (Max Heap):**
```cpp
priority_queue<int> pq;
pq.push(10);
pq.push(5);
pq.push(20);
cout << pq.top(); // 20
```

**Example (Min Heap):**
```cpp
priority_queue<int, vector<int>, greater<int>> pq;
pq.push(10);
pq.push(5);
pq.push(20);
cout << pq.top(); // 5
```
