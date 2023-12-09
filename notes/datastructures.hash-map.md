---
id: azirqu78s4pdbsosv0gqakm
title: Hash Map
desc: ''
updated: 1689523040829
created: 1682274863093
---


### interface

```cpp
template <typename K, typename V>
class HashMap {
public:
    // constructors
    HashMap();

    // destructor
    ~HashMap();

    // accessors
    V& operator[](const K& key);
    const V& operator[](const K& key) const;
    V& at(const K& key);
    const V& at(const K& key) const;
    bool contains(const K& key) const;

    // capacity
    int size() const;
    bool empty() const;

    // modifiers
    void insert(const K& key, const V& value);
    void remove(const K& key);
    void clear();
};
```