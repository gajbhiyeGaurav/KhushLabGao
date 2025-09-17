# C++ Full Notes

## 1. Introduction to C++
- **C++** is a general-purpose, object-oriented programming language developed by Bjarne Stroustrup.
- It is an extension of C with support for object-oriented programming, templates, and standard libraries.

## 2. Basic Structure of a C++ Program
```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!";
    return 0;
}
```
- `#include <iostream>`: Includes the standard input-output stream.
- `int main() { ... }`: Entry point of every C++ program.
- `std::cout`: Used to print output.
- `return 0;`: Ends the main function.

## 3. Data Types and Variables
- **Basic Data Types**: `int`, `float`, `double`, `char`, `bool`
- **Modifiers**: `short`, `long`, `unsigned`, `signed`
- **Declaring Variables**:
```cpp
int a = 10;
float b = 3.14;
char c = 'A';
bool flag = true;
```

## 4. Input/Output
```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Enter your age: ";
    cin >> age;
    cout << "Your age is " << age;
    return 0;
}
```

## 5. Operators
- **Arithmetic**: `+`, `-`, `*`, `/`, `%`
- **Relational**: `==`, `!=`, `<`, `>`, `<=`, `>=`
- **Logical**: `&&`, `||`, `!`
- **Assignment**: `=`, `+=`, `-=`, `*=`, `/=`
- **Increment/Decrement**: `++`, `--`

## 6. Control Structures

### If-Else
```cpp
if (condition) {
    // code block
} else {
    // code block
}
```

### Switch
```cpp
switch (expression) {
    case value1:
        // statements
        break;
    default:
        // statements
}
```

### Loops
- **For Loop**:
    ```cpp
    for (int i = 0; i < 10; ++i) { ... }
    ```
- **While Loop**:
    ```cpp
    while (condition) { ... }
    ```
- **Do-While Loop**:
    ```cpp
    do { ... } while (condition);
    ```

## 7. Functions

### Declaration and Definition
```cpp
int add(int a, int b) {
    return a + b;
}
int main() {
    int sum = add(5, 3);
}
```

### Default Arguments
```cpp
int sum(int a, int b = 5) { return a + b; }
```

### Function Overloading
```cpp
int sum(int a, int b);
double sum(double a, double b);
```

## 8. Arrays and Strings

### Arrays
```cpp
int arr[5] = {1, 2, 3, 4, 5};
```

### Strings
```cpp
#include <string>
string s = "Hello";
```

### Character Arrays
```cpp
char str[10] = "Hello";
```

## 9. Pointers

### Basics
```cpp
int a = 10;
int *p = &a;
```

### Pointer to Pointer
```cpp
int **pp = &p;
```

### Dynamic Memory Allocation
```cpp
int *arr = new int[5];
delete[] arr;
```

## 10. Object-Oriented Programming

### Classes and Objects
```cpp
class Student {
public:
    int age;
    void display() {
        cout << "Age: " << age;
    }
};

int main() {
    Student s;
    s.age = 20;
    s.display();
}
```

### Constructors and Destructors
```cpp
class Test {
public:
    Test() { cout << "Constructor"; }
    ~Test() { cout << "Destructor"; }
};
```

### Access Specifiers
- `public`, `private`, `protected`

### Inheritance
```cpp
class Animal {
public:
    void eat() { cout << "Eating"; }
};
class Dog : public Animal {
public:
    void bark() { cout << "Barking"; }
};
```

### Polymorphism (Function Overriding)
```cpp
class Base {
public:
    virtual void show() { cout << "Base"; }
};
class Derived : public Base {
public:
    void show() override { cout << "Derived"; }
};
```

### Abstraction and Encapsulation
- Abstraction: Hiding details, showing only essentials.
- Encapsulation: Binding data and methods together.

### Friend Function
```cpp
class A {
    friend void show(A&);
};
void show(A& obj) { ... }
```

## 11. Templates

### Function Template
```cpp
template <typename T>
T add(T a, T b) { return a + b; }
```

### Class Template
```cpp
template <class T>
class MyClass { ... };
```

## 12. Exception Handling
```cpp
try {
    // code that may throw
} catch (exception &e) {
    cout << "Error";
}
```

## 13. Standard Template Library (STL)

### Vectors
```cpp
#include <vector>
vector<int> v = {1, 2, 3};
v.push_back(4);
```

### Iterators
```cpp
for (auto it = v.begin(); it != v.end(); ++it) { ... }
```

### Other Containers
- `list`, `deque`, `stack`, `queue`, `map`, `set`, etc.

## 14. File Handling
```cpp
#include <fstream>
ofstream fout("file.txt");
fout << "Hello";
fout.close();

ifstream fin("file.txt");
string s;
fin >> s;
fin.close();
```

## 15. Advanced Topics

### Lambda Functions
```cpp
auto add = [](int a, int b) { return a + b; };
```

### Smart Pointers
```cpp
#include <memory>
unique_ptr<int> p1(new int(10));
shared_ptr<int> p2 = make_shared<int>(20);
```

### Namespaces
```cpp
namespace myns {
    int x = 10;
}
```

### Type Casting
- `static_cast`, `dynamic_cast`, `const_cast`, `reinterpret_cast`

### Preprocessor Directives
```cpp
#define PI 3.14
#ifdef PI
#endif
```

## 16. Best Practices
- Use proper naming conventions.
- Avoid memory leaks (prefer smart pointers).
- Use STL containers.
- Write modular code using functions and classes.
- Use comments to explain code logic.

---

## Resources to Learn More
- [cplusplus.com](https://www.cplusplus.com/)
- [GeeksforGeeks C++](https://www.geeksforgeeks.org/c-plus-plus/)
- [LearnCpp.com](https://www.learncpp.com/)

---

**If you want examples or explanation on any specific topic, let me know!**
