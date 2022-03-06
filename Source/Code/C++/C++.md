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

#### Subroutines: Reusable Blocks of Code


#### Object Oriented Coding


#### Pointers and Memory


#### Inheritance


#### Odds and Ends: Twos Complement and Static Variables


#### Developing a Program: The Particle Fire Simulation