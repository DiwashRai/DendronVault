---
id: 3xirn9y2ejhs5hgoh6ko9i1
title: Heap
desc: ''
updated: 1682275789077
created: 1682275626872
---


### interface
```cpp
template <typename T>
class Heap {
public:
    // constructors
    Heap();
    Heap(const Heap& other);
    Heap(Heap&& other);

    // assignment operators
    Heap& operator=(const Heap& other);
    Heap& operator=(Heap&& other);

    // move constructor and assignment operator
    Heap(Vector&& other);
    Heap& operator=(Vector&& other);

    // destructor
    ~Heap();

    // accessors
    T& top();
    const T& top() const;

    // capacity
    int size() const;
    bool empty() const;

    // modifiers
    void push(const T& value);
    void pop();
    void emplace(const T& value);
    void clear();
};
```