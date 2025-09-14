# STL (Standard Template Library) Notes

## Comparison of STL Containers

| Container | Size    | Random Access | Search | Insert | Erase |
|-----------|---------|---------------|--------|--------|-------|
| Array     | Fixed   | Yes           | O(n)   | O(n)   | O(n)  |
| Vector    | Dynamic | Yes           | O(n)   | O(n)   | O(n)  |
| Deque     | Dynamic | Yes           | O(n)   | O(1) (back/front) | O(1) (back/front) |
| Stack     | Dynamic | No            | No     | O(1) (push) | O(1) (pop) |
| Queue     | Dynamic | No            | No     | O(1) (back only) | O(1) (front only) |

---

## Vector Operations
- `push_back(x)`  
- `pop_back()`  
- `erase(v.begin() + i)`  
- `insert(v.begin() + i, x)`  

Illustration:  

```
begin()                               end()
  ↓                                    ↓
[  ][  ][  ][  ][  ]
```

---

## Deque Operations
- `push_back(x)`  
- `pop_back()`  
- `push_front(x)`  
- `pop_front()`  

---

## Stack Operations
- `push(x)`  
- `pop()`  
- `top()`  

---

## Queue Operations
- `push(x)`  
- `pop()`  
- `front()`  

---

## Standard Operations (Common)
- `size()`  
- `clear()`  
- `empty()`  
- `swap(v2)`  
