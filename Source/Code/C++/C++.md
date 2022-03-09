# C++
C++ is a general-purpose programming language created by Bjarne Stroustrup as an extension of the C programming language, or "C with Classes". The language has expanded significantly over time, and modern C++ now has object-oriented, generic, and functional features in addition to facilities for low-level memory manipulation. C++ was designed with an orientation toward systems programming and embedded, resource-constrained software and large systems, with performance, efficiency, and flexibility of use as its design highlights. C++ has also been found useful in many other contexts, with key strengths being software infrastructure and resource-constrained applications, including desktop applications, video games, servers (e.g. e-commerce, web search, or databases), and performance-critical applications (e.g. telephone switches or space probes).

#### Installation
- C++ was installed on Ubuntu 20.04 for VSCode using the instructions specified here (https://code.visualstudio.com/docs/cpp/config-linux)
- How to use CMake to handle build files and headers, as the VSCode instructions seem to mainly be for single files with everything in the same directory...(https://steelph0enix.github.io/posts/vscode-cpp-setup/)

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
- Best convention is to have the header files only contain the prototypes for each of the functions that you wish to use, with the definitions being religated to their own .cpp file. This is done so that functions are not defined multiple times in multiple locations.
In header file:
```c++
class Cat {
private:
	bool happy;
public: //accessable methods in the class
	void speak();
	void jump();
}
```
In .cpp file
```c++
void Cat::speak() {
cout << "Meow!" << endl;
}

void Cat::jump() {
cout << "Jumping to top of bookcase" << endl;
}
```
- The `::` assign the method to the class
In other .cpp file:
```c
int main() {
	Cat kitten; //instantiate variable kitten using class Cat
	
	kitten.speak(); //call method
	kitten.jump();
}
```

Data Members:
- .cpp files are converted into object files (.o) before being linked together. This is why headers consist of the prototypes for functions, as each object file can't see the other files yet
- want to make as much of the internal variables and methods of a class to be private as possible.
- variables initialized in a class will be given a random value, where you will want to use Constructors to assign a meaningful initial value.
		- You can set the initialize variable inside of the class when you define the class (i.e. `bool happy=true;`)

C++ Constructors and Destructors:
- A constructor is a method that will run when we instantiate the class variable
- The constructor must be the same name as the class and is public
- A destructor is a method that runs when the class variable is destroyed. This is done by leaving the scope in which the variable is usable (think after a function is done and it returns something, all those variables in the function are now deleted and their memory available for other purposes)
- destructors have the same name as the class, except with a `~` in front of them, and are public
- you can "aggressively use `{}`" to create scopes in a function. This is very uncommon, but can be used for advanced memory management.

In header file:
```c++
class Cat {
private:
	bool happy;
	string name;
public:
	void makeHappy();
	void makeSad();
	void speak();
	void jump();
	Cat(); //constructor
	~Cat(); //destructor
};
```
In .cpp file:
```c++
Cat::Cat() {
	cout << "Cat created" << endl;
	happy = true;
}

Cat::~Cat() {
	cout << "DESTRUCTOR ACTIVATED: Cat destroyed" << endl;
}

void Cat::speak() {
	if (happy) {
		cout << "Meow!" << endl;
	} else {
		cout << "HISSS!" << endl;
	}
}

void Cat::jump() {
	cout << "Jumping to top of bookcase" << endl;
}

void Cat::makeHappy() {
	happy = true;
}

void Cat::makeSad() {
	happy = false;
}
```


C++ Getters and Setters:
- Getters and Setters are just methods for getting and setting values. They aren't really special in any formatting way, just think of them as methods which change or return the variable values associated with a given instance of a class.
- Like below, which would change the `name` variable and return the `name` variable associated with a given instance of the `Cat` class
```c++
void Cat::setName(string newName) {
	name = newName;
}

string Cat::getName() {
	return name;
}
```
- These are controversial, as it can be thought of as exposing the private variables to outside influence.

C++ String Stream:
- String streams let you concatenate disparate types of data, like a double and a string into a single string
- streams are essentially streams of data that you can send data to or get data from
```c++
#include <iostream>
#include <sstream>

using namespace std;

int main() {
	string name = "Bob";
	int age = 32;
	
	stringstream ss;
	ss << "Name is; ";
	ss << name;
	ss << "; Age is: ";
	ss << age;
	
	cout << ss.str() << endl; // The .str() tells stringstream to return a string of the data it has been given
	
	//OR YOU CAN DO THIS:
	string info = ss.str();
	cout << info << endl;
	
}

```

Overloading Constructors:
- You can make constructors that intake parameters at the instantiation of the class as a variable
- The constructor with the matching input parameter types will be the one that is run when you instantiate
```c++
class Person {
private:
	string name;
	int age;
public:
	Person();
	Person(string new_name);
	Person(string new_name, int new_age);
	getname();
}

int main() {
	Person person1;
	Person person2("Bob");
	Person person3("Steve", 85);
}

Person::Person() {
	name = "Ross";
	age = 26;
}

Person::Person(string new_name) {
	name = new_name;
}

Person::Person(string new_name, int new_age) {
	name = new_name;
	age = new_age;
}

```

The "this" Keyword:
- `this->var1 = var1` inside of a method makes the `var1` on the left side refer to the `var1` which is shared across all of the class (in this specific instantiation)
- For example, in the code snippet below, inside of the `Person::Person` constructor, since the variables being passed in are `name` and `age` (which is the same name as the two variables already defined in the `private:` section and thus available to every part of the class), the constructor doesn't know which `name` and `age` you are referring to. The `this->` keyword is put before the variables available to every part of the class.
`this->name` corresponds to the variable declared in `private:`
`name` corresponds to the variable that only exists in the current scope
```c++
class Person {
private:
	string name;
	int age;
public:
	Person(string name, int age);
}

Person::Person(string name, int age) {
	this->name = name;
	this->age = age;
}

```
- It will be defined further when we get to pointers

Constructor Initialization Lists:
- A more efficient way of having constructors is to use initialization lists. These allow you to more efficiently change/assign the input parameters to the variables defined in the class:
- The below example is a re-writing of the above example but using initialization lists. `name(name)` effectively says `name = input_name`.
- If its small enough it isn't that frowned upon to just put the whole thing in the class protocol, as can be seen below with `Person(string name): name(name), age(0);`
```c++
class Person {
private:
	string name;
	int age;
public:
	Person();
	Person(string name, int age);
	Person(string name): name(name), age(0);
}

Person::Person(string name, int age): name(name), age(age) {
}
Person::Person(): name("unknown"), age(0) {
}

```


#### Pointers and Memory
Pointers:
- `int* variable` creates an "int pointer" or "pointer to an int" which can be used to store the address of a given variable. You can also type this as `int *variable` (or use other data types)
- Putting an `&` in front of a variable returns the address of the variable. The example below stores the address of `nValue` into the int pointer `pnValue`
		- It is a somewhat common practice to put  a `p` at the front of pointer variables
- You can "dereference" the pointer by typing an `*` in front of it to get the value that pointer refers to. This allows you to change what is stored at that address
- The example below passes the pointer to a variable in memory into a function. This means that a copy of the variable isn't made for the scope of the function, but rather a copy of its pointer. This allows for changes to be made to the variable by changing the value of the variable referenced by the address in the pointer.
```c++
#include <iostream>
using namespace std;

void manipulate(double *pValue) {
	cout << "2. Value of double in manipulate: " << *pValue << endl;
	*pValue = 10.0;
	cout << "3. Value of double in manipulate: " << *pValue << endl;
}

int main() {

	int nValue = 8;
	int *pnValue = &nValue;

	cout << "Int value: " << nValue << endl;
	cout << "Pointer to int address: " << pnValue << endl;
	cout << "Int value via pointer: " << *pnValue << endl;

	cout << "==================" << endl;

	double dValue = 123.4;

	cout << "1. dValue: " << dValue << endl;
	manipulate(&dValue);
	cout << "4. dValue: " << dValue << endl;
}
```


Arithmetic:
- When doing arithmetic in C++, the data type being used strongly influences the results. For example `int value1 = 7/3;` will set `value1` equal to 2. The `int` data type will remove any information after a decimal place.
		- However, even `double value1 = 7/3;` will set `value1` equal to 2. This is due to the fact that both `7` and `3` are `int` values, meaning their result will also be an `int`. This will remove all information after the decimal point before assigning it's value to `double value1`
		- You can get around this by having one of the value in the arithmatic be a `float` or `double`, or by "casting" one of the numbers as either a `float` or `double`
- `var += 1;` will add 1 to `var` and set that new value as `var`. The same with `var++;`
- `13%5` will divide 13 by 5 and return the remainder. This will be an `int` due to the reasoning discussed above
```c++
#include <iostream>
using namespace std;

/*
 * +
 * -
 * *
 * /
 * +=
 * -=
 * /=
 * *=
 * %
 * %=
 * precedence
 */

int main() {

	double value1 = (double)7/2;
	cout << value1 << endl; //3.5

	int value2 = (int)7.3;
	cout << value2 << endl; //7

	int value3 = 8;
	value3 += 1; // value3 = value3 + 1 or value3++;
	cout << value3 << endl; //9

	int value4 = 10;
	value4 /= 5; // value4 = value4/5
	cout << value4 << endl; //2

	int value5 = 13%5;
	cout << value5 << endl; //3

	double equation = ((5/4)%2)+(2.3*6); // follows PEMDAS (kind of)
	cout << equation << endl;
}
```

- General convention is to use parenthesis as often as possible for more complex equations to improve readability

Pointers and Arrays:

Pointer Arithmetic:

Char Arrays:

Reversing a String:

References:

The "const" Keyword:

Copy Constructors:


#### Inheritance


#### Odds and Ends: Twos Complement and Static Variables


#### Developing a Program: The Particle Fire Simulation