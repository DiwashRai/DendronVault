---
id: j6629ov8i69dg12ifxdbzqa
title: Queue
desc: ''
updated: 1682274579401
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

    // move constructor and assignment operator
    Queue(Vector&& other);
    Queue& operator=(Vector&& other);

    // destructor
    ~Queue();

    // accessors
    T& front();
    const T& front() const;
    T& back();
    const T& back() const;

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