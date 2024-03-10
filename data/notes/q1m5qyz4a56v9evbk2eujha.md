
## Summary
Prior to C++ 11, if you wanted to get an object from one place to another, you would have to create a throwaway object that you wanted to just pass into a function.
Move Semantics allows you to just move an object without creating unnecessary objects.

## Move constructor
- Point new object to old object's data
- Point old object to nullptr

## Move assignment operator
- Check 'other' object does not equal 'this'
```cpp
if (this == &other) return *this;
```
- delete current data
- point 'this.data' to 'other.data'
- return *this
