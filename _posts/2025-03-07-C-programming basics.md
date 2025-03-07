---
title: "C programming basics"
date: 2025-03-07 17:45:00 +04:00
categories: [Low Level Programming]
tags: ["C","Low Level programming"]
---
# C Programming Basics

## 1. Variables in C

### What is a Variable?
A variable in C is a named location in memory used to store data. It must be declared before use.

### Declaring Variables
Syntax:
```c
<datatype> <variable_name>;
```
Example:
```c
int age;
float salary;
char grade;
```

### Initializing Variables
Variables can be assigned values during or after declaration.
```c
int age = 25;
float salary = 50000.50;
char grade = 'A';
```

## 2. Data Types in C
C provides several data types:

| Data Type | Size (Bytes) | Description |
|-----------|-------------|-------------|
| `int`     | 4           | Stores integers (whole numbers) |
| `float`   | 4           | Stores floating-point numbers (decimals) |
| `double`  | 8           | Stores larger floating-point numbers |
| `char`    | 1           | Stores a single character |
| `void`    | 0           | Represents no value |

Example:
```c
int num = 10;
float pi = 3.14;
char letter = 'C';
```

## 3. `printf()` in C
The `printf` function is used to print output to the console.

### Syntax:
```c
printf("format string", variables);
```

### Format Specifiers:

| Specifier | Description |
|-----------|-------------|
| `%d`      | Integer (decimal) |
| `%f`      | Floating-point number |
| `%c`      | Character |
| `%s`      | String |


### Example:
```c
#include <stdio.h>
int main() {
    int age = 25;
    float salary = 50000.50;
    char grade = 'A';
    
    printf("Age: %d\n", age);
    printf("Salary: %.2f\n", salary);
    printf("Grade: %c\n", grade);
    return 0;
}
```

### Output:
```
Age: 25
Salary: 50000.50
Grade: A
```

## 4. `scanf()` in C
The `scanf` function is used to take input from the user.

### Syntax:
```c
scanf("format string", &variables);
```

### Example:
```c
#include <stdio.h>
int main() {
    int age;
    float salary;
    
    printf("Enter age: ");
    scanf("%d", &age);
    
    printf("Enter salary: ");
    scanf("%f", &salary);
    
    printf("Age: %d, Salary: %.2f\n", age, salary);
    return 0;
}
```

### Output (User Input):
```
Enter age: 30
Enter salary: 60000.75
Age: 30, Salary: 60000.75
```

### Note:
- The `&` (address-of) operator is required in `scanf()` except for strings.
- Be careful when mixing different data types to avoid input errors.

## 5. Summary
- Variables store data and must be declared with a type.
- C supports basic data types like `int`, `float`, `char`, etc.
- `printf()` prints output using format specifiers.
- `scanf()` reads user input and stores it in variables.

