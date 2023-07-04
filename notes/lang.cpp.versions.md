---
id: 3vtad9ehlxwa5n2gffrjsr1
title: Versions
desc: ''
updated: 1688495175611
created: 1688494431962
---

# C++ evolution through the years

## Pre 98
**Early evolution**:
- Bjarne Stroustrup started development of C++ in 1979 at Bell Labs as an enhancement to the C
language. It was originally named C with Classes but later it was renamed C++ in 1983.

**C with class**:
- **Classes**: Introduced user-defined types that encapsulate data and related functions.
- **Objects**: Allows creation of objects from classes.
- **Data abstraction**: Enabled separation of interface(public members) and implementation(private
members).
- **Member functions**: Functions that can be defined within the class definition and can access
the class's private and public members.
- **Inheritance**: Creation of new classes based on existing classes.
- **Constructors & destructors**
- **Operator overloading**
- **Type checking** during compilation
- **Inline functions**

## C++ 98
The first standardised version of the C++ language. Provided a consistent definition of the
language that all compilers could adhere to.

**Features**:
- **Templates**: Allowed definition of generic classes and functions making code more reusable
and flexible.
- **STL**: The standard template library - a powerful library of template classes and functions.
- **Namespaces**: Help organise code and prevent naming conflicts.
- **Exceptions**: Provide a way to handle error conditios separate to the main flow of program
control.
- **New casts**: (dynamic_cast, static_cast, reinterpret_cast, const_cast) Safer and more precise
alternative to C-style casts.
- **Boolean type**: 'true' and 'false'
- **RTTI**: Run-Time Type Information. Allows information about object's type to be retrieved
during runtime.
- **'auto_ptr' Smart Pointer**: Early version of the smart pointer
- **Internationalisation support**: Provided by the `<locale>` library.

## C++ 03
Essentially a 'bug fix' version of C++98. Did no introduce any major new features but focused on
correcting issues and ambiguities identified in C++98 standard.

The few minor features included were:
- **Value initialisation**: Used to ensure objects are intialised even if no explicit initialiser
is provided.
- **Library extensions**: STL was expanded with new functions and existing ones improved.
- **Exception specifications**: Clarifications to how exception specs worked. Included "throw
nothing" by using `throw()`.
- **Keyword `export`**: Difficult to implement and seldom used. Was since removed in C++11.

## C++ 11
Major update to C++ that had a host of new features and improvements. It was a significant
milestone in the evolution of C++ and made the language more modern, safer and expressive. It
changed the way programmers wrote code and improved perfomance of C++ applications.

The changes were significant enough that people refer to modern C++ as a different language to
compared to pre-C++11.

- **Rvalue references and Move semantics**: Allows 'moving' resources instead of copying them.
Can significantly imporove performance, particularly with alrge data structures.
- **Smart pointers**: New memory management tools: `shared_ptr`, `unique_ptr` and `weak_ptr`
- **Auto keyword**: Allows automatic type deduction which can make code more readable and easier
to maintain.
- **Nullptr keyword**: Replaces the ambiguous `NULL`.
- **Range-based for loops**: Simpler syntax to iterate over collections.
- **Initialiser lists**: A new way to initialise objects allowing more compact and intuitive code.
- **Lambda expressions**: Feature borrowed from functional languages that make it easier to use
function objects.
- **Concurrency support**: Native support for multithreading including threads, locks and condition
variables.
- **Type inference**: The `decltype` keyword was introduced, which deduces the type of an
expression
- **Strongly typed enums**: `enum class` was introduced which is more type-safe than normal enums.
- **Deleted and defaulted functions**: Allows for default generation of constructor and assignment
functions and to delete them when not required.
- **Variadic templates**: Allows creation of functions and classes with arbitrary number of
template parameters in a type-safe way.
- **User defined literals**: Enables more readable code by allowing user defined literals.

## C++ 14
A more minor release in comparison to C++11.

## C++ 17

## C++ 20

## C++ 23
