# 322_Assignment04 - Software Engineering
The purpose of this document is to compare formatting between C and Python.\
```Formatting output matters because it shows presentation and cleanliness in regards to updating the user about the document or code at hand, especially if a new update is rolled out.```

## Integer Formatting
### C99 Printf
```c
#include <stdio.h>

int main(){
    int num = 8;
    printf("Integer with padding, width, and sign: %+6d\n", num);
    return 0;
}
```
Output:\
Integer with padding, width, and sign:  +8
### Python Print
```python
# Do the same thing but with %.
num = 8
print("Integer with padding, width, and sign: %+6d" % num)

# Do the same thing but with fstrings.
num = 8
print(f"Integer with padding, width, and sign: {num:+6d}")
```
Output:\
Integer with padding, width, and sign:  +8\
Integer with padding, width, and sign:  +8
## Float Formatting
### C99 Printf
```c
#include <stdio.h>

int main(){
    float num = 8.0;
    float num2 = 8.88E3;
    printf("Float with padding, width, and sign: %+6.2f\n", num);
    printf("Float with padding, width, and sign: %+6.2f\n", num2);
    return 0;
}
```
Output:\
Integer with padding, width, and sign:  +8.00\
Integer with padding, width, and sign:  +8880.00
### Python Print
```python
# Do the same thing but with %.
num = 8.0
num2 = 8.88e3
print("Float with padding, width, and sign: %+6.2d" % num)
print("Float with padding, width, and sign: %+6.2d" % num2)

# Do the same thing but with fstrings.
num = 8.0
num2 = 8.88e3
print(f"Float with padding, width, and sign: {num:+6.2d}")
print(f"Float with padding, width, and sign: {num2:+6.2d}")
```
