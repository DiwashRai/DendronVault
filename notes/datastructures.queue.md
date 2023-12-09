---
id: j6629ov8i69dg12ifxdbzqa
title: Queue
desc: ''
updated: 1682366158862
created: 1682274477681
---


### interface

```cpp
template <typename T>
class Queue {
public:
    // constructors
    Queue();
    Queue(const Queue& other);
    Queue(Queue&& other);

    // assignment operators
    Queue& operator=(const Queue& other);
    Queue& operator=(Queue&& other);

    // destructor
    ~Queue();

    // accessors
    T& front();
    const T& front() const;
    T& back();
    const T& back() const;

    // capacity
    std::size_t size() const;
    bool empty() const;

    // modifiers
    void push(const T& value);
    void pop();
    template <typename... Args>
    void emplace(Args&&... args);
    void clear();
};
```