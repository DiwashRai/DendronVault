---
id: 9q02r7785re7jcvazvp6q54
title: Priority_queue
desc: ''
updated: 1678223250546
created: 1678223091389
---

### Default max queue syntax
```cpp
std::priority_queue<int> max_heap;
```

### To make it a min heap
```cpp
std::priority_queue<int, vector<int>, std::greater<int>> min_heap;
```