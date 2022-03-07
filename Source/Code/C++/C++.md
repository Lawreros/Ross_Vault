# C++
C++ is a general-purpose programming language created by Bjarne Stroustrup as an extension of the C programming language, or "C with Classes". The language has expanded significantly over time, and modern C++ now has object-oriented, generic, and functional features in addition to facilities for low-level memory manipulation. C++ was designed with an orientation toward systems programming and embedded, resource-constrained software and large systems, with performance, efficiency, and flexibility of use as its design highlights. C++ has also been found useful in many other contexts, with key strengths being software infrastructure and resource-constrained applications, including desktop applications, video games, servers (e.g. e-commerce, web search, or databases), and performance-critical applications (e.g. telephone switches or space probes).

#### Installation
- C++ was installed on Ubuntu 20.04 for VSCode using the instructions specified here (https://code.visualstudio.com/docs/cpp/config-linux)

#### Outline Structure inspiration
The outline for this note, and by extension the information about C++ is taken from the course *C++ Tutorial for Complete Beginners* found here (https://www.udemy.com/course/free-learn-c-tutorial-beginners/)


#### Further investigation:
- GDB debugger (see link in installation section)
- `g++` command used for creating the different file types that go into a C++ executable file
- The weird requirement that the referenced functions must go above `main`, unless you make a declaration statement that the function exists
- For new projects, if you want to make a new `tasks.json` file for compiling your project, see here https://stackoverflow.com/questions/34268034/where-is-the-tasks-json-file-in-vscode

#### Basic Syntax
- Variables
		- When naming variables, capitalization matters
		- Can't start a variable name with a number, but you can have numbers in the middle or end of variables
- Strings
		- `string` is technically a class, while `int` is a "primitive type"
		- strings are not completely standard between compilers
		- `"This puts a tab between this word \tand this word`

- User Input
		- `cout` is a special object for outputting text
		- `<<` is called the "insertion operator", they perform an operation (like `+`) that insert information into `cout`
		- `cin` object and the "extraction operator" `>>`

- Integer Types
		- `#include <limits>` allows for the use of `INT_MAX` and `INT_MIN` which are variables which contain the maximum and minimum numbers that can be represented by `int` for your compiler/system
		- `long int variable_name = ` allows you to make larger integers
		- `short int` allows you to save memory for your integers
		- `sizeof(int)` or `sizeof(variable_name)` returns number of bytes

- Floating Points
		- `float` allows for the use of decimal places
		- `double` is a larger `float` in terms of dedicated memory, so better significant figures
		- `cout` can print the value of a float, but add extra numbers at the end. This is not an issue with the variable, it's an issue with `cout`. `cout` just thinks "I will read the value of this variable to to a certain number of significant figures, if there aren't that many, I'll make some up to display"
		- after including the library `#include <iomanip>`in your program,  `cout << setprecision(10) << fixed << variable_name << endl;` sets the number of numbers after the decimal place that `cout` will try to show to 10

Other Types: Char and Bool
- `char` is meant to represent a single character from the ASCII library, so you can actually use numbers like `char variable = 27;`
- You can do something called "casting" which changes the data type that a variable is read as: `cout << (int)some_char_variable << endl;` will output the integer value of the character stored as `some_char_variable` instead of the character
- `wchar_t` allows for more characters to be represented (it is similar to what `double` is to `float`)

If Statement:
- Exactly what you think
- `if(condition) { }`

If-Else:
- only one option in a series of if-else statements will be run, namely the first one that program comes across that evaluates to `true`. You can't have multiple `else if` statements run.

Comparing Floats:
- Because `float`'s have garbage after a certain number of digits after the decimal place, you can't do something as simple as `if(value1 == 1.1) {...}'
- You can come up with a somewhat hacky solution with `if(value1 < 1.11) {...}`

C++ Conditions:
- `!=` "not equal"
- `<=` less than or equal to
- `>=` greater than or equal to
- `if(value1 == 7 && value2 == 4) {...}`
- `if(value1 == 7 || value2 == 4) {...}` This OR statement is checked from left to right, where if one of the conditions is found to be true the program doesn't check the remaining conditions
- `bool condition1 = (value1 == 8) && (value2 < 3)` will create the variable `condition` which is a bool for whether value1=8 and value2 < 3

While Loops:
- `while() {...}`
- `i++` increments `i` by 1, similar to python's `i =+ 1`

Do-While Loops:
- `do { ... } while();`
- difference from just a while loop is that the program is guaranteed to run the contents of the do-while loop at least once
- It executes code, then checks the while condition at the end to determine if another loop is needed. This is different from the while loop which will check before
- `const string` makes an immutable string
- variables only exist inside of the scope that they are defined in:
```c++
string input = "else";

// This loop will run infinitely, because the while loop
// checks the variable input that is in the global scope

while(input == "else") {
	string input = "something"; // different input variable
}

```

For Loops:
- `for(int i=0; i < 10; i++) {...}` creates a loop which starts with `i=0` and keep incrementally increasing `i` by 1 until `i<10` is evaluated to `false`
- `for(;;) {...}` creates and infinite loop

Break and Continue:
- `break;` breaks the innermost loop currently occuring
- `continue;` breaks out of particular iteration of the loop and starts the next loop

Arrays - Lists of Data
- `int values[3]` creates an array with 3 elements
		- `double values[3]`
		- `float values[3]`
		- `string values[3]`
- `int values[3] = {4, 35, 16};`
- `values[0] = 35;` assigns single element
- These values can be accessed the same way they are defined `x = values[0]`
- If you call an element of an array without first assigning it a value, you'll get a random value which is whatever the computer had in it's memory stored there
- If you initialize the array when you declare it, you don't need to define the number of elements in the array, the compiler will do that automatically: `string texts[] = {"one", "two", "three"};`
- IMPORTANT: There is nothing stopping you from accessing array elements that don't exist. These will return whatever is in the memory there. For example with `int values[3] = {1,2,3}` you can use `x = values[27]` without an issue. You can also write to elements that don't exist

Multidimensional Arrays
 ```c++
string animals[2][3] = {
	{"fox", "dog", "cat"},
	{"mouse","squirrel","parrot"}
};

for(int i=0; i<2; i++) {
	for(int j=0; j<3, j++) {
		cout << animals[i][j] << " " << flush;
	}
	cout << endl;
}
```

- C++ does rows, columns
- You can kind of cheese the creation of the array by just using a list of values. Both of the following variables make the same 3D array:
```c++
int test[2][3][4] = {3, 4, 2, 3, 0, -3, 9, 11, 23, 12, 23, 
                 2, 13, 4, 56, 3, 5, 9, 3, 5, 5, 1, 4, 9};


int test[2][3][4] = { 
                     { {3, 4, 2, 3}, {0, -3, 9, 11}, {23, 12, 23, 2} },
                     { {13, 4, 56, 3}, {5, 9, 3, 5}, {5, 1, 4, 9} }
                 };
```

Sizeof and Arrays
- `sizeof` is an operator that gives the number of bytes attributed to a variable in the memory
- You can use `sizeof(some_array)` to get the size of the array

Sizeof Multidimensional Arrays
- 

Switch
```c++
int value = 4;

switch(value) {
	case 4:
		cout << "Value is 4" << endl;
		break;
	case 5:
		cout << "Value is 5" << endl;
		break;
	default:
		cout << "Unrecognized value" << endl;
}
```
- `default` is not needed, the switch will just do nothing, but it is good practice to include
- If you don't include the `break;`, the program will go to the matching case and the keep executing all the way down. So in the above example, if `case 4` did not have a `break;` then it would run both `case 4:` and `case 5:` until reaching the `break;` in `case 5:`
- You are NOT allowed to have a variable as a `case` statement, only literals or constants (i.e. `const int value = 4;` and then `case value:`), so no `case some_variable: ...`

#### Subroutines: Reusable Blocks of Code
Functions:
- C++ is mainly focused on classes, and improvement on C which focused exclusively on functions
- The compiler reads things from top to bottom, so if a function is not declared before it is called, then the compiler will fail
- `void function() {...}`

Return Values:
- The data type you put before a function is called the "Return type"
- `int some_variable = some_function();`
- variables are dependent on the scope they are currently a part of

Function Parameters
- `void some_function(int variable1) {...}` can be called using `some_function(29);` or `some_function(variable);`
- When variables are passed into a function, a copy is made inside of the scope of the function. Changes only exist inside that scope.

Headers and Prototypes (NEED TO REVISIT HOW XCODE DOES HEADERS)
- You can declare functions before they have be defined by putting a "prototype" of the function above `main()`. So above `main()` you can put something like `void some_function();`. With that the compiler says "I trust that this function takes the inputs and returns the outputs that you say" and moves on, eventually getting to the definition
- headers get called using `#include "headerfile.h"`
- General rational is that `<>` around a header reference some file that is in a standard location that the compiler will know about, while `""` are usually used for files included in your project
- compiler literally copies the text in the header file and puts it at the top of you `.cpp` file
1)  preprocessor looks at the `#` symbols in your code and processes them
2)  compile the source code
3)  assemble the compiled files
4)  linking the object code file
- multiple includes for the same file in a program and prevented by the preprocessor and the `#ifndef` and `#define` commands in the header files


#### Object Oriented Coding
Classes:

Data Members:

C++ Constructors and Destructors:

C++ Getters and Setters:

C++ String Stream:

Overloading Constructors:

The "this" Keyword:

Constructor Initialization Lists:

#### Pointers and Memory


#### Inheritance


#### Odds and Ends: Twos Complement and Static Variables


#### Developing a Program: The Particle Fire Simulation