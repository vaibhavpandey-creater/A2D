# Ways to Swap Two Numbers in C++

In C++, there are several ways to swap two numbers. Here are some common methods:

## 1. Using a Temporary Variable

This is the most basic and straightforward way of swapping two numbers.

```cpp
int a = 5, b = 10;
int temp = a;
a = b;
b = temp;
```

## 2. Using Arithmetic Operations (Addition and Subtraction)

This method avoids the use of a temporary variable by utilizing arithmetic operations.

```cpp
int a = 5, b = 10;
a = a + b;  // a becomes 15
b = a - b;  // b becomes 5 (15 - 10)
a = a - b;  // a becomes 10 (15 - 5)
```

_Note: This method might lead to overflow issues if the numbers are too large._

## 3. Using Bitwise XOR

This method uses the XOR bitwise operation to swap numbers without using a temporary variable.

```cpp
int a = 5, b = 10;
a = a ^ b;  // a becomes 15 (5 XOR 10)
b = a ^ b;  // b becomes 5 (15 XOR 10)
a = a ^ b;  // a becomes 10 (15 XOR 5)
```

_Note: This method works for integer values and does not involve overflow issues._

## 4. Using std::swap() from the Standard Library

The C++ Standard Library provides a built-in function `std::swap()` to swap two variables.

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 10;
    swap(a, b);  // swaps the values of a and b
    return 0;
}
```

_This is the easiest and most efficient way to swap values in C++._

## 5. Using a Function

You can create your own function to swap two numbers using any of the above methods.

```cpp
void swapNumbers(int &a, int &b) {
    int temp = a;
    a = b;
    b = temp;
}

int main() {
    int a = 5, b = 10;
    swapNumbers(a, b);
}
```

## 6. Using Tuple (C++11 and Later)

With C++11, you can use `std::tuple` and `std::tie` to swap variables.

```cpp
#include <tuple>

int a = 5, b = 10;
std::tie(a, b) = std::make_tuple(b, a);
```

## Summary:

- **Temporary variable**: Basic and simple.
- **Arithmetic operations**: Avoids extra space, but risks overflow.
- **XOR**: No temporary space, but might be less readable.
- **std::swap**: Simple and efficient.
- **Function**: Can be used with custom logic.
- **Tuple**: Convenient with C++11 or newer.

All of these methods are common ways to swap two numbers in C++.
