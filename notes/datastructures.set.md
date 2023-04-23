---
id: wu8egj9yesx6l8j3odpa6br
title: Set
desc: ''
updated: 1682275539143
created: 1682275233912
---

### interface

```cpp
template <typename T>
class Set {
public:
    // constructors
    Set();

    // destructor
    ~Set();

    // modifiers
    void insert(const T& value);
    void remove(const T& value);
    void clear();

    // Operations
    bool contains(const T& value) const;
    T* find(const T& value) const;
    int count(const T& value) const;

    // capacity
    int size() const;
    bool empty() const;
};
```