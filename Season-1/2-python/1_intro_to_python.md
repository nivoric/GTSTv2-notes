## Whats is a programming language?
- It is a language which helps to communicate with computers, they are not able to understand human languages.
- We humans have a lot of languages like English, French, Mandarin, Arabic, Amharic, etc. Computers also have a lot of languages like Assembly, C, C++, Java, JavaScript, Python and much more.
- Programming languages help us to write programs that computers understand.

## What is a program?
- A program is an algorithm expressed in a programming language. An algorithm is a detailed sequence of actions to accomplish some task, Named after the Iranian mathematician, **Al-Khawarizmi**.
- Technically, an algorithm must reach a result after a finite number of steps. With those steps, programs do a specific task correctly.

### Pseudo code 
- Pseudo code is a simplified, structured way of writing down programming logic in plain language. Without worrying about the syntax of a specific programming language.
- It uses short, clear statements to outline each step of a program's logic, making it easier for beginners to understand how an algorithm works and for programmers to plan complex solutions before writing actual code. 
- You can use any informal language, the main concern is breaking the process down. You can literally write the code in any way that you can understand.
- Example of pseudo code for a simple login process:

```bash
BEGIN 
    PROMPT user for username
    PROMPT user for password
    IF username and password match
        DISPLAY "Login Successful"
    ELSE
        DISPLAY "Login Failed"
END
```

## Evolution of I/O {Input/Output}
- Early in the history of computing, programs were submitted on punch cards with all the data they required and executed together with other programs that used the same libraries. Output was to a line printer.
- Later developments introduced interactive processing which allows the user to provide data while the program was running. This normally takes place in a question and answer format.

### Generation of computers
1. **First Generation**: Vacuum Tubes => punch cards.
2. **Second Generation**: Transistors => programming started here with Assembly.
3. **Third Generation**: Integrated Circuits => BASIC, COBOL, Pascal, Fortran, C, C++, Perl and Ada.
4. **Fourth Generation**: Microprocessors => Python, SQL, MatLab.
5. **Fifth Generation**: Artificial Intelligence.
- They could only solve one problem at a time. It would take days or even weeks to set up a new program on first generation. Which means if they screwed up something, they should redo from the beginning.

## Types of programming languages
- Computers understand binary (0/1), humans don't understand this. So based on the closeness of the language to humans we classify it into 2: 
    1. **Low-level** = less close to human language, but works faster than high-level.
    2. **High-level** = more close to human language, but works slower than low-level.

### 1. Low-level languages.
- These languages are more like machines but with lots of effort people can understand them. They are close to the hardware of the computer, more than that of High-level languages.
- Example: Assembly, C-lang, etc...

### 2. High-level languages.
- They are more close to human languages, but not close to the computer's hardware like that of Low-level languages.
- Example = Python, C++, Java, JS, etc...

#### How do high-level languages work?
- As we saw earlier, we have said that computers know only binary, and if we code with high-level languages, how do computers understand us?
1. **Compilers** = are tools which helps to convert the whole code to byte-code then the computer will execute it.
    - Example = C, C++, Java...
2. **Interpreter** = can directly execute the code by reading the source code line by line.
    - Example = Python.

## Uses of programming languages
- Android Application Development 
- Website Development 
- Machine Learning
- Artificial Intelligence
- Game Development
- Big Data technology
- Desktop software development 
- Hacking tool development

## Python programming 
- Python is a high-level & interpreted programming language. Also, it is very easy to learn.
- It is a very simplified language anyone can learn it and it is almost the same as plain English.
- Python was developed by **Guido Van Rassum** in the late 1980s and early 1990s at the national research institute for mathematics and computer science in the Netherlands. Python is derived from many other languages including **ABC, Modula-3, C, C++, Algol-68, SmallTalk and Unix shell** and other scripting languages.
- Python is now maintained by a core development team at the institute, although Guido Van Rassum still holds a vital role in directing it's progress.

### Uses of Python
- Data visualization,
- Data analysis,
- Machine Learning,
- Artificial Intelligence,
- Back-end web development with frameworks like Django and Flask,
- Game development,
- Hacking tool development,
- Scripting and much more...

### IDE & Code editors
- IDE (Integrated Development Environment): Is a software that helps to write & run a specific programming language. Example: Python IDE 
- Code editors: are softwares those can help to write any kind of programming languages and also by adding some compiling/Interpreting feature they can run programs/scripts. 
- Example: Sublime, VScode.

### Outputs and Comments
- On python, to display output  we use keyword 'print'
- Syntax = `print('term/output')`.
- You can use the term "Display" for pseudo code.
- use "\n" for new line and "\t" for tab space. Examples are shown below in the code block.
- **Comments** = these are simple notes written on our codes, those can help as to remember the function of the code or to make it simple for other to understand our code. Commands won't be executed in the code.
- Syntax = `# this is how you write comments`.

```python
# We use hashtags to write one lined comments.
# when we wanna write multiple lines of comments we can use triple quotes like this:
'''
This is a multiple
line comment section
which any body in python can use.
'''

# using input() to take user input
num = input('Enter a number: ')

print('You entered:', num)

print('Data type of num is:', type(num))

print('hello \t there')
# output = hello    there

print('hello \n world')
'''
your output would be like this:
hello
 world
'''
```

### Python keywords
- **Keywords** are pre-defined, reserved words used in python programming that have special meanings to the compiler. The main ones are:

```python
False, None, True, and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield.
```

### Variables
- Variables are a value holders/containers. They store data, we give some value to some word.

```python
Example:
number = 10 -> from now on python knows the value of number is 10 unless changed.
```

- The process of giving value to word is called ==Variable Declaration==. You can use this term when writing pseudo code by saying "Declared".

```python
gtst = 10
print(gtst)
# output = 10

# Pseudo code for Variable declaration
DECLARE "gtst" with value 10 -> gtst = 10.
```

- You can print out a variable's value with the following methods:

```python
gtst = 10

# this is methodd 1
print("You are",gtst,"years old")
# output = You are 10 years old.

# This is method 2
print("You are {gtst} years old")
```

- **Rules**:
	- Don't use space between words, instead use an underscore
	- Don't use numbers as identifier

```python
my name = "zido" -> # This will take only "name" as the variables.
12 = "zido" -> # Numbers can't be used as variables/value holders.
```

### Data types in python
- There a lot of data types in python, the main ones:
1. **Numeric** = the numeric data type in python includes the *int(integers), float(decimals) and complex(complex numbers)* classes. This basically holds numeric values.
2. **String** = This holds a sequence of characters.
3. **Sequence** = the sequence data type in python includes the *list, tuple, range* classes. This data type can be called by index numbers. This basically holds collection of items.
	1. **List** = ordered collection of similar or different types if items separated by commas and enclosed within square brackets [ ]. 
		- to access items from a list, we use the index numbers (0, 1, 2, 3, 4,...). it is shown below as an example in the code block.
	2. **Tuple** = ordered sequence of items same as list. The only difference is that tuples are immutable, you can't add using `append` like lists. 
		-  We use parenthesis( ) to store items of a tuple. Similar to lists, we use index numbers to access tuple items.
4. **Mapping/Dictionary** = Is an unordered collection of items. holds data in key-value pair form. We use **keys** to retrieve the respective value. But not the other way around. This type of data doesn't have an order so it doesn't get called by index numbers.
5. **Boolean** = Basically either *True* or *False*.
6. **Set** = the set data type in python includes the *set* and *frozen-set* classes. basically holds a collection of unique items.

```python
# Numeric data
num1 = 5    # this is an integer number
print(type(num1))
num2 = 10.3 # this is a float number
print(type(num2))
num3 = 1+2k # this is a complex number
print(type(num3))

# String data
name = 'Python'
print(name) # output: Python
message = 'Python is for beginners'
print(message) # output: Python is for beginners

# Boolean data
print(3>1) # output: True
print(3<1) # output: False

# Sequnce data
## A. List
languages = ['Swift', 'Java', 'Python']
print(languages[0]) # prints out 'Swift'
print(languages[2]) # prints out 'Python'
language.append("Amharic") # use this to add elements to the list
print(languages) # prints out the languages with Amharic.

## B. Tuple
product = ('Microsoft', 'Xbox', 499.99)
print(product[0]) # Microsoft
print(product[2]) # 499.99

# Mapping/Dictionary
capital_city = {'Nepal':'Kathmandu', 'Italy':'Rome', 'England':'London'}
print(capital_city['Nepal']) # output: Kathmandu.
print(capital_city['Kathmandu']) # prints out an error message.
```

