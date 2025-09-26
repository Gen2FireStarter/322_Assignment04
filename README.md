# 322_Assignment04 - Software Engineering
The purpose of this document is to compare formatting between C and Python.\
```Formatting output matters because it shows good presentation and cleanliness in regards to updating the user about the document or code at hand, especially if a new update is rolled out.```

## Integer Formatting
### C99 Printf
```c
#include <stdio.h>

int main(){
    int num = 8;
    printf("Integer with padding, width, and sign: %+6d\n", num);
    printf("Integer with padding, width, and sign: %6d\n", num);
    printf("Integer with padding, width, and sign: %06d\n", num);
    return 0;
}
```
Output:\
Integer with padding, width, and sign:  +8\
Integer with padding, width, and sign:  8\
Integer with padding, width, and sign:  00008
### Python Print
```python
# Do the same thing but with %.
num = 8
print("Integer with padding, width, and sign: %+6d" % num)
print("Integer with padding, width, and sign: %6d" % num)
print("Integer with padding, width, and sign: %06d" % num)

# Do the same thing but with fstrings.
num = 8
print(f"Integer with padding, width, and sign: {num:+6d}")
print(f"Integer with padding, width, and sign: {num:+d}")
print(f"Integer with padding, width, and sign: {num:06d}")
```
Output:\
Integer with padding, width, and sign:  +8\
Integer with padding, width, and sign:  8\
Integer with padding, width, and sign:  00008

Integer with padding, width, and sign:  +8\
Integer with padding, width, and sign:  8\
Integer with padding, width, and sign:  00008

## Float Formatting
### C99 Printf
```c
#include <stdio.h>

int main(){
    float num = 8.0;
    printf("Float with padding, width, and sign: %+6.2f\n", num);
    printf("Float with padding, width, and sign: %06.2f\n", num);
    printf("Float with padding, width, and sign: %e\n", num);
    return 0;
}
```
Output:\
Float with padding, width, and sign:  +8.00\
Float with padding, width, and sign:  000008.00\
Float with padding, width, and sign:  8.0e+1
### Python Print
```python
# Do the same thing but with %.
num = 8.0
print("Float with padding, width, and sign: %+6.2f" % num)
print("Float with padding, width, and sign: %06.2f" % num)
print("Float with padding, width, and sign: %e" % num)

# Do the same thing but with fstrings.
num = 8.0
print(f"Float with padding, width, and sign: {num:+6.2f}")
print(f"Float with padding, width, and sign: {num:06.2f}")
print(f"Float with padding, width, and sign: {num:e}")
```
Output:\
Float with padding, width, and sign:  +8.00\
Float with padding, width, and sign:  000008.00\
Float with padding, width, and sign:  8.0e+1

Float with padding, width, and sign:  +8.00\
Float with padding, width, and sign:  000008.00\
Float with padding, width, and sign:  8.0e+1
## String Formatting
### C99 Printf
```c
#include <stdio.h>

int main(){
    char a* = "This is a test."
    printf("%-10s!\n", a);
    printf("%10s!\n", a);
    return 0;
}
```
Output:\
"This is a test.              "\
"              This is a test."
### Python Print
```python
    a = "This is a test."
    b = "This is also a test."
    print("%10s!" % a)
    print("%10s!" % a)

    print(f"{a:<10}")
    print(f"{a:>10}")
    print(f"{a:^10}")
    print(a + " " + b)
```
Output:\
"This is a test.              "\
"              This is a test."\
"     This is a test.         "\
"This is a test."
## Tables
| Type | Example Code (C) | Example Code (Python) | Output |
|---|---|---|---|
| Int | ``` printf("%6d\n", 8); ``` | ``` print("%6d" % 8) ``` | 8 |
| Int | ``` printf("%+6d\n", 8); ``` | ``` print("%+6d" % 8) ``` | +8 |
| Int | ``` printf("%06d\n", 8); ``` | ``` print("%06d" % 8) ``` | 00008 |
| Float | ``` printf("%6.2f\n", 8); ``` | ``` print("%6.2f" % 8) ``` | 8.00 |
| Float | ``` printf("%e", 8.0); ``` | ``` print("%e" % 8.0) ``` | 8.0e+1 |
| String | ``` printf("%10s!", "Hello!"); ``` | ``` print("%10s!" % "Hello!") ``` | "Hello !"
| String | ``` printf("%-10s!", "Hello!"); ``` | ``` print("%-10s!" % "Hello!") ``` | "Hello!"
## Links
[C99 printf reference](https://en.cppreference.com/w/c/io/fprintf)\
[Python old-style % formatting](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)\
[Python f-strings](https://docs.python.org/3/reference/lexical_analysis.html#f-strings)
