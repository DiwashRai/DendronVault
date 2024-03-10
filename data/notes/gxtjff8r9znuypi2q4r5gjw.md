
### Summary
`std::any` is a type-safe container for single values of any type introduces as part of C++17.
It can be thought of as a safer and more convenient alternative to `void*`. It is similar to
`std::variant` but it can hold any type, not just types specified in the template parameters.

std::any is useful when you need a variable that can hold any type, but you don't know the types at
compile time. However, it is generally better to avoid such situations if possible, because it
makes your code more error-prone and harder to understand. If you find yourself using std::any a
lot, it might be a sign that your code could benefit from more polymorphism or a redesign of your
data structures.

### Typical usage
#### Hetereogeneous vector
std::any is useful when you need a variable that can hold any type, but you don't know the types at
compile time. For example, you might want to create a container that can hold values of any type.

```cpp
std::vector<std::any> v;
v.push_back(12);
v.push_back(3.14f);
v.push_back(std::string("hello"));
```

### Examples
#### Basic usage
To retrieve the value from std::any, you need to know the type of the value, and you can use
std::any_cast to get it:
```cpp
#include <iostream>
#include <any>

int main() {
  std::any a;
  a = 12;
  std::cout << std::any_cast<int>(a) << '\n';
  a = 3.14f;
  std::cout << std::any_cast<float>(a) << '\n';
  a = std::string("hello");
  std::cout << std::any_cast<std::string>(a) << '\n';
}
```


#### std::bad_any_cast
Calling `std::any_cast` with the wrong type will throw a `std::bad_any_cast` exception.
```cpp
std::any a;
try {
  std::cout << std::any_cast<float>(a) << '\n';
} catch (const std::bad_any_cast& e) {
  std::cout << e.what() << '\n';
}
```

#### std::any_cast
`std::any_cast` can also be used to check if an `std::any` holds a particular type.
```cpp
std::any a = 12;
if (std::any_cast<int>(&a)) {
  std::cout << "a holds an int\n";
}
```

#### std::any_cast with references
`std::any_cast` can also be used to get a reference to the value held by an `std::any`.
```cpp
std::any a = 12;
int& i = std::any_cast<int&>(a);
i = 42;
std::cout << std::any_cast<int>(a) << '\n';
```
#### has_value and reset
`std::any` has a `has_value` method that returns true if it holds a value and false otherwise.
It also has a `reset` method that clears the value it holds.
```cpp
std::any a = 12;
std::cout << std::boolalpha << a.has_value() << '\n';
a.reset();
// now a doesn't hold a value
std::cout << std::boolalpha << a.has_value() << '\n';
```