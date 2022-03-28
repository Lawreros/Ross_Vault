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
- You can put multiple things in the last section of the for loop in order to have multiple things change per iteration. `for(int i=0; i<10; i++, j++)` will increase the value of both `i` and `j` by 1 at each iteration.
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
- string objects can actually be considered as pointers to where the string is actually stored. That's why strings of different lengths have the same size when you are using `sizeof(string)`. You aren't getting the size of the word, but rather the size of the address of the word.
- array variables and pointers are similar in nature, with the difference being that the array variable knows the size of the data it is pointing at. That is why `sizeof(array)` works.
- You can assign an array to a pointer, as the array variable is effectively just pointing to where each chunk of data is located in memory
- By adding 1 to a pointer, C++ knows that you want it to display the next block of data in the memory that it is pointing at.
- 
```c++
// Loop through an array using a pointer, with array element reference syntax
// Loop through an array by incrementing a pointer
// Loop through an array, stopping by comparing two pointers

int main() {

	string texts[] = { "one", "two", "three" };

	string *pTexts = texts; //makes the pointer *pTexts point to first entry in texts

	for (int i = 0; i < sizeof(texts) / sizeof(string); i++) {
		cout << pTexts[i] << " " << flush; //You can increment through the array by using the pointer like an array
	}

	cout << endl;

	for (int i = 0; i < sizeof(texts) / sizeof(string); i++, pTexts++) {//Adding +1 do pTexts tells C++ to go to next string entry in memory for the array
		cout << *pTexts << " " << flush;
	}

	cout << endl;

	string *pElement = &texts[0]; //set pointer to location for first entry
	string *pEnd = &texts[2]; //set pointer to locaton for last entry

	while(true) {
		cout << *pElement << " " << flush;

		if(pElement == pEnd) {//Stop when pointer locations are the same(?)
			break;
		}

		pElement++;
	}
}
```

Pointer Arithmetic:
- You can use addition and subtraction with pointer and locations in memory to creatively navigate through memory
```c++

int main() {
	const int NSTRINGS = 5;
	string texts[NSTRINGS] = {"one", "two", "three", "four", "five"};

	string *pTexts = texts;

	pTexts += 3;

	cout << *pTexts << endl;

	pTexts -= 2;

	cout << *pTexts << endl;

	string *pEnd = &texts[NSTRINGS];
	pTexts = &texts[0];

	while(pTexts != pEnd) {
		cout << *pTexts << endl;
		pTexts++;
	}

	// Set pTexts back to start.
	pTexts = &texts[0];

	long elements = (long)(pEnd - pTexts);

	cout << elements << endl;

	// Set pTexts back to start.
	pTexts = &texts[0];

	pTexts += NSTRINGS/2; //because NSTRINGS is an int, 2.5 is stored as 2 and added to pTexts
	cout << *pTexts << endl; //returns "three" because pTexts originally pointed to "one", then moved two locations down to "three" in the memory

}
```

Char Arrays:
- You can create an array of `char`'s and call it using `cout`
- `char text[] = "hello"` creates an array where `hello` is split up into individual character entries
- "null string terminator" is an invisible character at the end of the string which tells the computer that the string ends there. When you put a string in `""` the terminator is added.
		- This means that is you do `char text[] = "hello";` and then `sizeof(text)`, you will get `6` characters instead of `5` because the last entry in the array is the null string terminator (which you can cast to an `int` to see that it is a `0`)
```c++
int main() {
	char text[] = "hello";
	
	for(int i=0; i<sizeof(text); i++) {
		cout << i << ": " << text[i] << endl;
	} //returns 1: h, 2: e, 3: l, 3: l, 4: o, 5: 
	
	int k=0;
	
	while(true) {
		if(text[k] == 0)
			break;
		
		cout << text[k] << flush;
		k++;
	}
}
```

Reversing a String:
- weirdly enough, and interview question
- This is just one way of doing this, there are multiple other ways
- The excerpt below shows how to do it with pointers, another way is doing it with char arrays:
```c++
int main() {
	char text[] = "hello";
	int nChars = sizeof(text)-1;
	
	char *pStart = text;
	char *pEnd = text + nChars -1;
	
	while(pStart < pEnd) {
		char save = *pStart;
		*pStart = *pEnd;
		*pEnd = save;
		
		pStart++;
		pEnd--;
	}
	
	cout << text << endl;
	
}
```

References:
- `int &value2 = value1;` creates a reference, where changes made to `value2` also change `value1`. Think of `value2` being made into a synonym for `value1`
- "Reference variables create aliases to existing variables"
- Useful when you want to have a function that changes the value of something without using a `return` statement
- simpler to use a reference instead of a pointer when applicable

```c++

void changeSomething(double &value) {
	value = 123.4;
}


int main() {
	int value1 = 8;
	int &value2 = value1;
	value2 = 10;
	
	cout << "Value1: " << value1 << endl;
	cout << "Value2: " << value2 << endl;
	// Value1: 10
	// Value2: 10
	
	double value = 4.321;
	changeSomething(value);
	cout << value << endl;
	// 123.4
}
```

The "const" Keyword:
- `const` makes a variable no longer a variable. It can't change anymore.
- Common practice to make constants all caps to emphasize that it is a constant.
- Putting `const` in a class method between the `()` and `{}` makes it so that the method is unable to change any variable value. This is generally used as a safety precaution to make sure that classes are exactly what you say they are.
```c++
class Animal {
private:
	string name;

public:
	void setName(string name) { this->name = name; };
	void speak() const { cout << "My name is: " << name << endl; }
};

int main() {

	const double PI = 3.141592;
	cout << PI << endl;

	Animal animal;
	animal.setName("Freddy");
	animal.speak();

	int value = 8;

	// const int * const pValue = &value;
	int *pValue = &value;

	cout << *pValue << endl;

	int number = 11;
	pValue = &number; // Error with this: int * const pValue = &value;
	*pValue = 12; // Error with this: const int *pValue = &value;

	cout << *pValue << endl;
}
```

```c++
int value = 8;
const int *pValue = &value; //A pointer to a constant int
int* const pValue = &value; //A constant pointer to an int

const int* const pValue = &value; //A constant pointer to a constant int

```

Copy Constructors:
- A "copy constructor" is a special construction for C++ that is used when you set one variable of a class equal to an existing variable of the same class. The parameters of the existing variable are used to create the new variable, meaning that the new one isn't constructed the same way. (i.e. it doesn't call the constructor of the class mentioned in previous lessons)
- You can create your own copy constructors using references and `const`, passing in the existing class variable
		- Because the new variable is of the same class as what you are using, you can actually access `private` variables and assign values to them
- You can call `const` methods in a copy constructor because you know it doesn't change any values of the object. You don't want to be modifying the variable you are copying while you are copying it.

```c++
class Animal {
private:
	string name;

public:
	Animal() { cout << "Animal created." << endl; };
	Animal(const Animal& other): name(other.name) { cout << "Animal created by copying." << endl; };
	void setName(string name) { this->name = name; };
	void speak() const { cout << "My name is: " << name << endl; }
};

int main() {

	Animal animal1;

	animal1.setName("Freddy");

	Animal animal2 = animal1; //call copy constructor
	animal2.speak();
	animal2.setName("Bob");

	animal1.speak();
	animal2.speak();

	Animal animal3(animal1); //another valid way to call the copy constructor
	animal3.speak();

}
```

The New Operator:
- the `new` operator instantiates a variable from a variable type/class and must be referred to by a pointer. Variables created this way do not get deleted when going out of scope, as they aren't really associated with any scope. (apparently adds variable to the heap)
- always call `delete` when you call `new`, which will cause memory leaks because of the lack of a scope association
- look at the `this` description from before to see what the `->` means. It allows you to call methods on a pointer.
```c++
class Animal {
private:
	string name;

public:
	Animal() {//constructor
		cout << "Animal created." << endl;
	}

	Animal(const Animal& other) ://copy constructor
			name(other.name) {
		cout << "Animal created by copying." << endl;
	}

	~Animal() {//destructor
		cout << "Destructor called" << endl;
	}

	void setName(string name) {
		this->name = name;
	}

	void speak() const {
		cout << "My name is: " << name << endl;
	}
};


int main() {
	Animal *pCat1 = new Animal();
	pCat1->setName("Freddy");
	pCat1->speak();
	delete pCat1;

	cout << sizeof(pCat1) << endl;

}
```

Returning Objects from Functions:
- using `new` allows you to make objects with no real scope. This means that you can pass around the pointer to the object without worrying about the object getting deleted as the function ends, or returning a copy of the object (the copy constructor is called if an object is returned by a function, as the program that called the function is assigning a copy of the returned variable to a new variable in its scope and deleting the returned variable)
- you can specify functions to return pointers
- Remember, you need to call `delete` to prevent memory leaks when passing around objects.

```c++
class Animal {
private:
	string name;

public:
	Animal() {
		cout << "Animal created." << endl;
	}
	Animal(const Animal& other) :
			name(other.name) {
		cout << "Animal created by copying." << endl;
	}
	~Animal() {
		cout << "Destructor called" << endl;
	}
	void setName(string name) {
		this->name = name;
	}
	void speak() const {
		cout << "My name is: " << name << endl;
	}
};

Animal *createAnimal() { //returns a pointer to an Animal variable
	Animal *pAnimal = new Animal();
	pAnimal->setName("Bertie");
	return pAnimal;
}

int main() {
	Animal *pFrog = createAnimal();
	pFrog->speak();
	delete pFrog;
}
```


Allocating Memory:
- `new` both allocates enough memory for the object and instantiates the object in that spot
- putting `[]` after a `new <object type>` statement allows you to determine how many of that object you want to create. This is treated like an array, aka a collection of pointers, and can be accessed and interacted as such.
		- You must then do `delete [] <array_name>` to tell C++ that you aren't just deleting one instance of the object that the pointer points at
- 

```c++
class Animal {
private:
	string name;

public:
	Animal() {
		cout << "Animal created." << endl;
	}

	Animal(const Animal& other) :
			name(other.name) {
		cout << "Animal created by copying." << endl;
	}

	~Animal() {
		cout << "Destructor called" << endl;
	}

	void setName(string name) {
		this->name = name;
	}

	void speak() const {
		cout << "My name is: " << name << endl;
	}
};


int main() {

	Animal *pAnimal = new Animal[10];

	pAnimal[5].setName("George");
	pAnimal[5].speak();

	delete [] pAnimal;

	char *pMem = new char[1000];
	delete [] pMem;

	char c = 'a';
	c++; //can use arithematic with characters
	string name(5, c); //"create a string with 5 characters, with the character being the value of c"
	cout << name << endl; //bbbbb
}
```

Arrays and Functions:
- You loose information about the number of elements in an array when you pass it into a function, as if you ask for the size all you get is the size of the pointer (in function `show1` if you did `sizeof(texts)`, you would get the size of a string pointer)
		- It's common practice to also pass in the number of elements in the array

- If you do want to retain size information, you have to pass a pointer to the array (`show3`). You have to put `&texts` in brackets to make it a "reference to an array of strings". If you didn't do that it would be considered an "array of references to strings"
- You can return an array from a function through the use of pointers, but you don't want to return pointers to local variables in that scope (the local variable will be deleted and now you pointer points to nothing). Use of `new` is pretty much required
		- Note that you can't specify to a function that you are returning an array. Remember that you have to put the return type in front of the function, and there is not type for an array.
- Can declare variables outside of any function, they'll be available to every function

```c++
// Could declare variables here! string numbers[] = {"one", "two", "three"};

void show1(const int nElements, string texts[]) {

	// cout << sizeof(texts) << endl; returns sizeof pointer!

	for(int i=0; i<nElements; i++) {
		cout << texts[i] << endl;
	}
}

void show2(const int nElements, string *texts) {

	// cout << sizeof(texts) << endl; returns sizeof pointer!

	for(int i=0; i<nElements; i++) {
		cout << texts[i] << endl;
	}
}

void show3(string (&texts)[3]) {//have to specify number of elements in array

	// cout << sizeof(texts) << endl; returns sizeof pointer!

	for(int i=0; i<sizeof(texts)/sizeof(string); i++) {
		cout << texts[i] << endl;
	}
}

char *getMemory() {
	char *pMem = new char[100];

	return pMem;
}

void freeMemory(char *pMem) {
	delete [] pMem;
}

int main() {
	string texts[] = {"apple", "orange", "banana"};

	cout << sizeof(texts) << endl;
	
	show1(3, texts);
	show2(3, texts); //show1, show2, and show3 are equivalent
	show3(texts);
	
	char *pMemory = getMemory();
	freeMemory(pMemory);

}
```

Namespaces:
- namespaces are a way of avoiding conflicts between classes and variables with the same name
- You can put header information and .cpp information in a namespace by putting all of the text inside of `namespace <some_name> {...}`
		- You must put both inside of a namespace, if the header or definition is in a namespace, the other must be
- If you have more than on namespace, you must specify the namespace if you have identically named classes'
- Without a header file with a definition of what is inside of the namespace, the program does not know that the namespace exists. Thus you must include the relevant header.
- As long as the namespace is defined, you don't have to expressly say `using namespace cats`, you can just do `cats::`
- You can define variables and constants in namespaces

main.cpp
```c++
#include <iostream>

#include "Animals.h"
#include "Cat.h"

using namespace std;
using namespace jwp;

int main() {

	Cat cat;
	cat.speak();

	jwp::Cat cat2;
	cat2.speak();

	cats::Cat cat3;
	cat3.speak();

	cout << jwp::CATNAME << endl;
	cout << cats::CATNAME << endl;

	cout << CATNAME << endl;

	return 0;
}

```

Animals.cpp
```c++
#include "Animals.h"

namespace jwp {

Cat::Cat() {
	// TODO Auto-generated constructor stub
}

Cat::~Cat() {
	// TODO Auto-generated destructor stub
}

void Cat::speak() {
	cout << "Sssssss!" << endl;
}

} /* namespace jwp */
```

Animals.h
```c++
#ifndef ANIMALS_H_
#define ANIMALS_H_

#include <iostream>
using namespace std;

namespace jwp {

const string CATNAME = "Tiddles";

class Cat {
public:
	Cat();
	virtual ~Cat();
	void speak();
};

} /* namespace jwp */

#endif /* ANIMALS_H_ */
```

Cat.cpp
```c++
#include "Cat.h"

namespace cats {

Cat::Cat() {
	// TODO Auto-generated constructor stub
}

Cat::~Cat() {
	// TODO Auto-generated destructor stub
}

void Cat::speak() {
	cout << "Meuuowww!" << endl;
}

}
```

Cat.h
```c++
#ifndef CAT_H_
#define CAT_H_

#include <iostream>
using namespace std;

namespace cats {

const string CATNAME = "Freddy";

class Cat {
public:
	Cat();
	virtual ~Cat();
	void speak();
};

}
#endif /* CAT_H_ */
```

#### Inheritance
Inheritance: 
- "sub/child classes" are a type of the "super-class"
- Allows you to extend the methods accessible to the sub-class from the existing methods of the super-class
- You can have sub-classes made from sub-classes. It really just comes down to what information is available to each level of sub

```c++
class Animal {
public:
	void speak() { cout << "Grrr" << endl;}
};

class Cat: public Animal {
public:
	void jump() { cout << "Cat jumping!" << endl; }
};

class Tiger: public Cat {
public:
	void attackAntelope() { cout << "Attacking!" << endl;}
};

int main() {
	Animal a;
	a.speak();
	
	Cat cat;
	cat.speak();
	cat.jump();
	
	Tiger tiger;
	tiger.jump();
	tiger.speak();
	tiger.attackAntelope();
}

```

Encapsulation:
- Encapsulation is the idea that you want to make as much of the variable values and methods private as possible in a class
- It's common practice to make a `private:` section in the class for variables and another for methods/functions (this doesn't effect how the code runs, it's just more readable.)

```c++
class Frog {
private:
	string name;
	
private:
	string getName() { return name; }
	
public:
	Frog(string name): name(name) { }
	
	void info() { cout << "My name is:" << endl;}
};

int main() {
	Frog fron("Freddy");
	frog.info();
}
```


Constructor Inheritance:
- for a sub class, the constructor of the parent class is called before the constructor of the sub class
- while a subclass can not access a private variable of a parent class, it can access methods of the parent class that can access private variables
- you can set up a constructor of a subclass so that it has access to private variables of a parent class by having the constructor call the parent constructor
		- You can only have a subclass constructor use its immediate parent's constructor, you can skip multiple levels

```c++
class Machine {
private:
	int id;
	
public:
	Machine(): id(0) { cout << "Machine no-argument constructor called." << endl; }
	Machine (int id): id(id) { cout << "Machine parameterized constructor called." << endl; }
	void info() { cout << "ID: " << id << endl; }
};

class Vehicle: public Machine {
public:
	Vehicle(int id): Machine(id) { cout << "Vehicle parameterized constructor called." << endl; }
	Vehicle() { cout << "Vehicle no-argument constructor called." << endl;}
}:

class Car: public Vehicle {
public:
	Car(): Vehicle(999) { cout << "Car no-argument constructor called" << endl; }
};

int main() {
	Car car;
	car.info();
}
```


#### Odds and Ends: Twos Complement and Static Variables
Twos Complement:
- Talk about the "wrap around" thing that happens when you exceed the value that can be stored for a variable.
- Look up `One's Complement` and `Two's Complement` as memory storage techniques. These are how you can can store numbers to do arithmetic easily with binary. `One's Complement` is outdated and not commonly used.
```c++
int main() {
	char value = 127; //maximum value that can fit in a char

	cout << (int)value << endl;

	value++; // exceed maximum value

	cout << (int)value << endl; // prints "-128"
}
```

Static Keyword:
- `static` variables are shared across all objects of a particular class.
- `static` variables can only be accessed using `static` methods
- often used to keep track of how many times you've instantiated a class. You can use this to create a type of id for each object by using that static value with constructor methods.
- `id = count++;` assigns the value of `count` to `id` then increases `count` by 1. `id = ++count;` increases the value of `count` by 1, then assigns the value of `count` to `id`
```c++
// .h header file
class Test {
public:
	// Initialisation of const must be done right here!
	static int const MAX = 99;

private:
	int id;
	static int count;

public:
	Test() {
		id = count++; //assign value of count to id, then increase count by 1
	}

	int getId() {
		return id;
	}

	static void showInfo() {
		cout << count << endl;
	}
};

// .cpp source
int Test::count = 7;

int main() {

	Test::showInfo(); // displays 7
	cout << Test::MAX << endl; //displays 99

	Test test1;
	cout << "Object 1 ID: " << test1.getId() << endl; //displays 7

	Test test2;
	cout << "Object 2 ID: " << test2.getId() << endl;//displays 8

	Test::showInfo();
}
```

#### Developing a Program: The Particle Fire Simulation