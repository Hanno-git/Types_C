

##### int & float

- integer numbers truncate `(5 / 9 = 0.55 -> 0. -> 0)`!
- floating-point numbers do NOT truncate (double or float)

***


##### C Data Types

```c
char            //1 byte     -128 to 127 or 0 to 255
unsigned char   //1 byte      0 to 255
signed char     //1 byte      -128 to 127
int             //4 bytes     -2,147,483,648 to 2,147,483,647
unsigned int    //4 bytes     0 to 4,294,967,295
float           //4 byte	Value range - 1.2E-38 to 3.4E+38	Precision - 6 decimal places
double          //8 byte	Value range - 2.3E-308 to 1.7E+308	Precision - 15 decimal places
```

***
example 1: declare a constant string and 
```c
#include <string.h>

const char string[] = "Hello World";

int main(void)
{
char string_ch1 = string[0]; //string_ch1 = 'H'
char string_ch11 = string[10]; //string_ch1 = 'd'
char string_ch12 = string[11]; //string_ch1 = undefined behavior could be any value
string[0] = string_ch11; //string = "dello World"
int string_len = strlen(string); //string_len = 11
}
```
***
##### Standard Way of function declarations

Main function: `int main(void) {}`

Other functions: `int f(){}` becomes `int f(void){}`

***



##### Symbolic constants

A #define line defines a symbolic name or symbolic constant to be a particular string of characters:

```c
#define   NAME   replacement_text
```
therefore
```c
#define   NAME   replacement_text

int NAME = 100;
```
is the same as 
```c
#define   NAME   replacement_text

int replacement_text = 100;
```

- any occurrence of name (not in quotes and not part of another name) will be replaced by the corresponding replacement text
- The replacement text can be any sequence of characters; it is not limited to numbers


***
