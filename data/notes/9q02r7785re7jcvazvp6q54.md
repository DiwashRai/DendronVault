
### Default max queue syntax
```cpp
std::priority_queue<int> max_heap;
```

### To make it a min heap
```cpp
std::priority_queue<int, vector<int>, std::greater<int>> min_heap;
```