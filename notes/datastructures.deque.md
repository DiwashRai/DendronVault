---
id: pixne08f9hda3vzcetj2jvv
title: Deque
desc: ''
updated: 1682276469252
created: 1682276327212
---

### interface

```cpp
template <typename T>
class Deque {
public:
    // constructors
    Deque();
    Deque(const Deque& other);
    Deque(Deque&& other);

    // destructor
    ~Deque();

    // accessors
    T& front();
    const T& front() const;
    T& back();
    const T& back() const;
    T& operator[](int index);
    const T& operator[](int index) const;
    T& at(int index);
    const T& at(int index) const;

    // capacity
    int size() const;
    bool empty() const;

    // modifiers
    void push_front(const T& value);
    void push_back(const T& value);
    void pop_front();
    void pop_back();
    void emplace_front(const T& value);
    void emplace_back(const T& value);
    void clear();
};
```