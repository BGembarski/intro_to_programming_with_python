## Introduction
This guide is meant as an introduction to not only Python, but programming in
general. This guide will cover setting up your development environment as well
as basic data structures, data types, and programming concepts. Each lesson
will provide an introduction the a specific programming concept as well as some
exercises to build familiarity. Lessons will build off of each other, so make
sure you're sure you understand each concept before moving on to the next lesson.
While the lessons build off of each other, the exercises will not, so if you're
already familiar with a concept feel free to skip that lesson.

## Setting up your development environment
**Install Python**  
The first step is to install Python. This guide will use Python 2.7 and the
starter code will be in Python 2.7, so it is important you install the correct
version.

Installation instructions for Python can be found [here.](https://wiki.python.org/moin/BeginnersGuide/Download)  
Follow the instructions for your operating system.

Once you've installed Python open either terminal or command prompt and run
the following command to verify your installation.

```bash
python --version
```

You should see Python 2.7 in the output.

**Text Editor/Integrated Development Environment (IDE)**  
Now that you've installed Python, you need either a text editor or an IDE to
write code! Text editors are a light-weight way of editing code and often
have a wide variety of extensions to provide additional functionality of your
choice such as syntax highlighting and [linters.](https://en.wikipedia.org/wiki/Lint_(software) IDEs are more resource
intensive to run, but come with built-in features that make it easy to execute
your code and manage your projects. If you're comfortable using the terminal
I recommend you use a text editor, otherwise it will likely be easier to start
out using an IDE.

|Software|Type|Description|Installation|
|--------|----|-----------|
|Wing|IDE|Wing is an excellent IDE for learning python. It enables you to write and run your code in the same place which will enable you to focus on coding.| [install](https://wingware.com/downloads/wingide-personal)|
|Atom|Text Editor|Atom is an open source [electron](https://electron.atom.io/) based text editor with plenty of packages that allow you to customize your experience.|[install](https://atom.io/)|
|VS Code|Text Editor| Like Atom, VS Code is an open source text editor with numerous extensions that enable you to customize your editor. |[install](https://code.visualstudio.com/)|
|Sublime Text| Text Editor | Sublime is another popular text editor, but it is closed source and will constantly prompt you to buy the full version. Sublime also has numerous extensions that allow you to customize your experience.|[install](https://www.sublimetext.com/)|

## Lessons

### Lesson 1 - Simple Data Types
There are three main simple data types that are used extensively in programming.

**Integers**  
Integers are essentially whole numbers. Integers are useful when you don't need
precision. Integers also don't behave the same way they do in mathematics. Integers
effectively ignore the remainder when performing division.

Example:
```python
x = 5
y = 2
result = x / y
```
In the sample code above you would expect the value of result to be 2.5, right?
The actual value of result is 2. This is because integer division ignores remainders.
The value of 5 divided by 2 is 2 with a remainder of 1, so integer division ignores
the remainder and stores the whole number value.

**Floating Point Numbers**  
Floating point numbers are useful when you need more precision than whole numbers
allow. For example, when calculating percentages or dollar amounts. Floating point
numbers are roughly equivalent to decimal numbers in math.

Example:
```python
x = 5.0
y = 2.0
result = x / y
```
As you might expect, the value of result is 2.5.

What happens when you divide and integer by a floating point number or when you
divide a floating point number by an integer? What is the value of result in the
example below?

Example:
```python
x = 5.0
y = 2
result = x / y
```
If you guessed 2.5, you're right! When an operation mixes floating point numbers
an integers together, the result is a floating point number. The process through
which one data type is coerced to another is called casting. When a floating point
number is divided by an integer, the result is casted to a floating point number.
This casting occurs with all operations: division, multiplication, addition, and subtraction.

**Booleans**  
Booleans are a very simple data type, they have two possible values; True or False.
Booleans are useful for checking conditions and are used to control the path of
execution your program takes. You will see how useful booleans are in the lessons
covering if statements and loops. Booleans can be represented as conditions or
they can simply be assigned a value of True or False.

Example:
```python
x = 5
y = 5
z = 2
bool_true = (x == y)
bool_false = (x == z)
bool_also_false = (bool_false and bool_true)
bool_also_true = (bool_false or bool_true)
```
The example above shows how booleans can be combined to express complex conditions.
The 'and' keyword will evaluate to True if and only if the boolean expressions it
combines both evaluate to True. The 'or' keyword will evalue to True if either of
the expressions it combines evaluates to True. Boolean comparisons between numbers
can be used to check if the values are equivalent or not. Note that boolean
comparisons between numbers use '==' rather than the assignment operator '='.
Boolean comparisons aren't limited to '==', however. The table below shows all
the possible types of boolean operators and what they mean.

|Operator|Meaning|
|--------|-------|
|==| Equal to|
|!=| Not equal to|
|>| Greater than|
|<| Less than|
|>=| Greater than or equal to|
|<=| Less than or equal to|

**Exercises**  
The exercises for this lesson can be found in the lesson_one directory. Download
the files and open them in your IDE or text editor.

### Lesson 2 - If Statements
### Lesson 3 - While Loops
### Lesson 4 - For Loops
### Lesson 5 - Functions
### Lesson 6 - Classes
