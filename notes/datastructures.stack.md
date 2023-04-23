---
id: xgleienln5stv551d6l7qv6
title: Stack
desc: ''
updated: 1682274350191
created: 1682266168140
---


### interface

```cpp
template <typename T>
class Stack {
public:
    // constructors
    Stack();
    Stack(const Stack& other);
    Stack(Stack&& other);

    // assignment operators
    Stack& operator=(const Stack& other);
    Stack& operator=(Stack&& other);

    // move constructor and assignment operator
    Stack(Vector&& other);
    Stack& operator=(Vector&& other);

    // destructor
    ~Stack();

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

private:
    Vector<T> data;
};
```