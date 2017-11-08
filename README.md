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
choice such as syntax highlighting and [linters.](https://en.wikipedia.org/wiki/Lint_(software)) IDEs are more resource
intensive to run, but come with built-in features that make it easy to execute
your code and manage your projects. If you're comfortable using the terminal
I recommend you use a text editor, otherwise it will likely be easier to start
out using an IDE.

|Software|Type|Description|Installation|  
|--------|----|-----------|------------|
|Wing|IDE|Wing is an excellent IDE for learning python. It enables you to write and run your code in the same place which will enable you to focus on coding.| [install](https://wingware.com/downloads/wingide-personal)|  
|Atom|Text Editor|Atom is an open source [electron](https://electron.atom.io/) based text editor with plenty of packages that allow you to customize your experience.|[install](https://atom.io/)|  
|VS Code|Text Editor| Like Atom, VS Code is an open source text editor with numerous extensions that enable you to customize your editor. |[install](https://code.visualstudio.com/)|  
|Sublime Text| Text Editor | Sublime is another popular text editor, but it is closed source and will constantly prompt you to buy the full version. Sublime also has numerous extensions that allow you to customize your experience.|[install](https://www.sublimetext.com/)|  

## Lessons
### Lesson 1 - Variables
Variables are one of the most basic concepts in programming. A variable is
essentially a data store that you can reference by name. Variables are assigned
using the assignment operator '=' and can be re-assigned at any time. Once a
variable has been assigned, the value within the variable can be used by
referencing the variable.

Example:
```python
# variable x is assigned the value of 5
x = 5
# variable  y is assigned the  value of x
y = x
# print out the value of both of the variables
print x
print y
```
**Exercises**   
The exercises for this lesson can be found in the lesson_1 directory. Download
the files and open them in your IDE or text editor.

Ex 1. - Create and assign a variable with the name 'length' and assign it the
value 10. Run the program to verify your output.

Expected Output:
```bash
Length is 10
```

### Lesson 2 - Simple Data Types
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
# Evaluates to True
bool_true = (x == y)
# Evaluates to False
bool_false = (x == z)
# Evaluates to False
bool_also_false = (bool_false and bool_true)
# Evaluates to True
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
The exercises for this lesson can be found in the lesson_2 directory. Download
the files and open them in your IDE or text editor.

Ex 1. - Create and assign a variable with the name 'divisor' such that it divides
the variable 'dividend' so that the result is 2. Save the result in a variable
named 'result'

Expected Output:
```bash
Result is 2
```

Ex 2. - Modify the first exercise so that 'divisor' is a floating point number.

Expected Output:
```bash
Result is 2.2
```

Ex 3. - Assign values to the enumerated values such that the printed expression
evaluates to True.

Expected Output:
```
Expression is True
```

### Lesson 3 - If Statements
If statements allow you to control what code gets executed. If statements enable
your program to branch - taking one path if a condition is true or taking a
different path if the expression is false. If statements use booleans to
determine which path to take.

Example
```python
x = 6
if x == 5:
  print "x is 5"

print "done"
```
In the above example the code snippet printing the value of x will only be run
if the value of x is 5, but the print statement at the end will always run no
matter what the value of x is since it is outside of the if statement.

What if you want to check for multiple values of x?
Easy!
```python
x = 6
if x == 5:
  print "x is 5"
elif x == 6:
  print "x is 6"
elif x == 7:
  "x is 7"

print "done"
```
The above example will first evaluate the expression x == 5 to False, then it
will check the next expression x == 6 which evaluates to True. Once one
expression in an if block evaluates to True and a branch is chosen, the other
expressions in the if-block will not be evaluated. For instance, in the previous
example the condition x == 7 is never checked since x == 6 evaluated to True.
The output of the example above is:
```
x is 6
done
```

It is also possible to write a condition that only executes if all other
conditions evaluate to False. This can be done using the keyword 'else'

Example
```python
x = 6
if x == 5:
  print "x is 5"
else:
  print "x is not 5"

print "done"
```

The output of this snippit is:
```
x is not 5
done
```

**Exercises**  
Ex 1. - The variable 'random_value' is randomly assigned a value between 1 and
10 (inclusive). Write an if statement block that prints 'value is low' if
random_value is in the range 1-3, 'value is medium' if random_value is in the
range 4-6, and 'value is high' if random_value is in the range 7-10.

Don't forget that you can combine multiple conditions into one expression
using the 'and' and 'or' keywords. Also don't forget about the '<' and '>'
boolean operators. See if you can re-write your if statement block multiple ways
and still get the correct output.

### Lesson 4 - Complex Data Types
Simple data types are useful, but it's hard to create any complex behavior
without some more complex data types. This section will introduce you to
lists, strings, sets, and dictionaries (known as maps in other languages).

**Lists**  
Lists are useful when you want to store multiple values in one variable. Lists
enable you to store an ordered set of 'variables' without needing a reference to
each individual item in the list.

This is how you create a list:
```python
# Create a list with 3 integers in it
integer_list = [1, 3, 2]
```

You can also create an empty list:
```python
my_list = []
```

And you can add elements to list like this:
```python
my_list = []
my_list.append(5)
# These two lines are equivalent to: my_list = [5]
```

To access items of a list, you need to access the index of an item. An index is
just a number that refers to which item in the list you want. In computer science
index numbers start at 0.

```python
integer_list = [1, 3, 2]
# Indices ->    0  1  2

# to access a list item, use this syntax
one = integer_list[0]
two = integer_list[1]
three = integer_list[2]
```
[Click here for more information on list operations](https://docs.python.org/2/tutorial/datastructures.html)

**Strings**  
Strings are a special case of lists. They are essentially a list of characters.
A character is just what you'd expect, an ASCII or unicode character.

Example String
```python
sample_string = "text here"
# sample_string is really a list -> ['t', 'e', 'x', 't', ' ', 'h', 'e', 'r', 'e']
```

Just like lists, strings can be accessed using an index with the same syntax.
```python
sample_string = "text here"
letter_x = sample_string[2]
```
The example above stores the value 'x' in the variable 'letter_x'

[Click here for more information on string operations](https://docs.python.org/2/library/string.html)

**Sets**  
Sets are containers just like lists, except they don't guarantee order and
they disallow duplicate entries. Sets are useful when you want to determine
if you've encountered an element before since checking if an object is a
member of a set is a very fast operation. Sets are also useful for determining
all unique items in a collection since they don't allow duplicates.

This is how you create a set:
```python
from sets import Set
my_set = Set()
```

You can add an element to a set like this:
```python
from sets import Set
my_set = Set()
my_set.add(5)
```

You can remove an element from a set like this:
```python
from sets import Set
my_set = Set()
my_set.add(5)
my_set.remove(5)
```

Checking if an element is in a set using the 'in' keyword:
```python
from sets import Set
my_set = Set()
my_set.add(5)
# checking if an element is in a set returns a boolean value
this_is_false = (6 in my_set)
this_is_true = (5 in my_set)
```

[Click here for more information on set operations](https://docs.python.org/2/library/sets.html)

**Dictionaries**   
Dictionaries are a set of key and value pairs. Just like sets, a dictionary
can't have duplicate keys and looking up a key is a fast operation. Dictionaries
allow you to map a value for each key. Dictionaries are useful whenever you need
the functionality of a set, but you also want to store an associated piece of
information with each element in a set. For instance, you could use a dictionary
to determine all unique items in a collection as well as the number of times each
element occurred.

You can create a dictionary like this:
```python
my_dictionary = {}
```

Adding a key-value pair to a dictionary is easy:
```python
my_dictionary = {}
my_dictionary['my key'] = 'my value'
```

You can retrieve the value for a given key using the same syntax:
```python
my_dictionary = {}
my_dictionary['my key'] = 'my value'
my_value = my_dictionary['my key']
# my_value now holds the string 'my value'
```

Checking if a key is in a dictionary can be done with the same syntax as sets:
You can retrieve the value for a given key using the same syntax:
```python
my_dictionary = {}
my_dictionary['my key'] = 'my value'
this_is_true = ('my key' in my_dictionary)
```

[Click here for more information on dictionary operations](https://docs.python.org/2/tutorial/datastructures.html#dictionaries)

**Determining the size of a complex data type**
You will often find that it is useful to know the size of a list, string, set, or
dictionary. Checking the size of a complex data type can be done using Python's
built in 'len()' function.

This is how you use len to check the size of a list, string, set, or dictionary:
```python
my_list = [1, 2, 3]
my_list_size = len(my_list)
# my_list_size now holds the integer value 3 since my_list has 3 elements
```

**Exercises**
### Lesson 5 - While Loops
### Lesson 6 - For Loops
### Lesson 7 - Functions
### Lesson 8 - Classes
