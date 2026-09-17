# Topics
- [ ] indexing and slicing (stat, stop, step)
- [ ] input handling (2 methods)
- [ ] operations/operators
- [ ] indentation
- [ ] if... else/conditional statements
- [ ] Errors(exceptions)
- [ ] Error handling
- [ ] loops
## Indexing
- On lists, we have seen about index numbers. We use them to access items from the list/tuple.

```python
languages = ['Python', 'Swift', 'JS']
print(languages[0]) # output: Python
```

- There is also something called **negative indexing**. based on the list 'Languages' shown above in the code block.

| index type/item   | Python | Swift | C++ |
| ----------------- | ------ | ----- | --- |
| Normal Indexing   | 0      | 1     | 2   |
| Negative indexing | -3     | -2    | -1  |

- The list index always starts with 0. Hence, the first element of a list is present at index 0, not 1. Calling texts by indexes also works for strings and tuples.

## Slicing
- In python, it is possible to access a section of items from the list using the slicing operator '==:==', not just a single item.
- **Slicing** is indexing syntax that extracts a portion from a list. If 'a' is a list, then `a[m:n]` returns the portion of 'a':
	- Starting with position 'm'.
	- Up to but not including 'n'.
	- Negative indexing can also be used.
- This is more applicable for strings.

```python
name = 'no 1 is zido'
print(name[8:12:1])
# output: zido.
```

- Python uses default step as 1, sometimes no need to tell/put it.
- Also default stopping index is the final, still no to for this kinda purpose.
- There are more writing features:

```python
# Example 1
name = 'No 1 is Nathan'
print(name[8:14]) # starting with index 8, up to index 14 (without including it) with no skipping/steps.
# output: Nathan

# Example 2
name = 'No 1 is Nathan'
print(name[8:]) # starting with index 8 up to the very end (including the end) with no skipping/steps.
## output: Nathan

# Example 3 - with lists
countries = ['Ethiopia','KSA','India','Nigeria']
print(countries[::]) # starting at index 0 up to the very end (including the end) with no skipping/steps.
## output: ['Ethiopia','KSA','India','Nigeria']

# Example 4 - List with negative index in the slicing
fruits = ['apple','banana','papaya','avocado']
print(fruits[1:-1:2]) # starts with index 1, ending at index -1 without including it and also skipping two indices.
## output: ['banana']
```

- More info about indexing and steps (both normal and negative ones):

| Indexing/steps    | apple | banana | papaya | avocado |
| ----------------- | ----- | ------ | ------ | ------- |
| normal indexing   | 0     | 1      | 2      | 3       |
| negative indexing | -4    | -3     | -2     | -1      |
| normal steps      | 1     | 2      | 3      | 4       |
| negative steps    | -4    | -3     | -2     | -1      |

## User Input handling
- On python, there are 2 types of inputs:
	- **By using the input function** and
	- **By Arguments**.
1. **By input function**:
	- Syntax = `var = input("Text you like to displat")`.
	- Will accept the input and stores it on variable.
	- You can change the input type to `int(), float(), eval(), str()...`.
```python
name = input("What is your name?\n=> ")
print(f"Hello {name}!")

# output: 
## What is your name?
## => zido
## Hello zido!
```
2. **Arguments**:
	- This helps us to get the input from the command lines
	- Shell: `python gtst.py arg1 arg2 arg3`.

```python
import sys
name = sys.argv[1]
print(f"Hell0 {name}")

# shell input: python3 test.py zido(arg1) ahmed(arg2)
# output: Hello zido!
# The reason python only accepted "zido", You have entered arg1 only and python memorizes zido as arg1 and ahmed as arg2.
# But when written in quotations like "zido ahmed", python takes all as arg1.
```
## Operators
- Operators are special symbols that perform operations on variables and values. 

```python
# for example
print(11 - 9) # output: 2
```

- There are a lot of operator types in python:
### 1.  Arithmetic Operators:
- They are simple maths operations. Inputs have to be in `int, eval and float` only.

| Operator | Operation      | Example       |
| -------- | -------------- | ------------- |
| +        | Addition       | `5 + 2 = 7`   |
| -        | Subtraction    | `4 - 2 = 2`   |
| *        | Multiplication | `2 * 3 = 6`   |
| /        | Division       | `4 / 2 = 1`   |
| %        | Modulus        | `5 % 2 = 1`   |
| 2 *      | Power          | `4 ** 2 = 16` |  

- The power operator has 2 astericks.

### 2. Assignment Operators:
- Assignment operators are used to assign values to variables.  You do the arithmetic operators first and then use the equal sign.

| Operator | Name                      | Example               |
| -------- | ------------------------- | --------------------- |
| =        | Assignment Operator       | `a = 7`               |
| +=       | Addition Assignment       | `a += 1, a = a + 1`   |
| -=       | Subtraction Assignment    | `a -= 1, a = a - 1`   |
| * =      | Multiplication Assignment | `a *= 1, a = a * 1`   |
| /=       | Division Assignment       | `a /= 1, a = a / 1`   |
| %=       | Remainder Assignment      | `a %= 1, a = a % 1`   |
| 2* =     | Exponent Assignment       | `a **= 1, a = a ** 1` |

- The multiplication assignment has an asterick and an equal sign next to each other.
- The exponent assignment has 2 astericks with an equal sign next to each other.

### 3. Comparison Operators:
- Used to compare variable and return boolean results. 
- Boolean means either **True or False**.

| Operator | Meaning                  | Example         |
| -------- | ------------------------ | --------------- |
| ==       | is equal to              | `3 == 5, False` |
| !=       | Not equal to             | `3 != 5, True`  |
| >        | Greater than             | `3 > 5, False`  |
| <        | Less than                | `3 < 5, True`   |
| >=       | Greater than or equal to | `3 >= 5, False` |
| <=       | Less than or equal to    | `3 <= 5, True`  |

### 4. Logical Operators:
- They are used to check if an expression is **True or False**.
- They use truth tables to compare.

| Operator | Example   | Meaning                                                                   |
| -------- | --------- | ------------------------------------------------------------------------- |
| and      | `a and b` | Logical AND: `True` only if both a and b are True                         |
| or       | `a or b`  | Logical OR: `True` if at least one of the operands (a and b) are True     |
| not      | `not a`   | Logical NOT: Inverts the current condition = True to false and vice versa |

- Truth table for the `AND` Operator

| A     | B     | A and B |
| ----- | ----- | ------- |
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

- Truth table for the `OR` Operator:

| A     | B     | A or B |
| ----- | ----- | ------ |
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

- Truth table for the `NOT` Operator:

| A     | Not A |
| ----- | ----- |
| True  | False |
| False | True  |

### 5. Bitwise Operators:
- Computers work with binaries, on our computer everything have a binary value (also called a bit)
- On python there is a keyword called `bin(Your_decimal)`, this helps to show you the binary value of your Decimal.
- **True has a value of 1, while False has a value of 0**.
- Bitwise operators are used to do maths on the binary value of expressions
- When dealing with Bitwise operators, you can add 0 in the front if the binary is not a 4-digit binary
- They are:
	- Compliment (Not) (~): opposite + 1.
	- And (&):  both must agree.
	- Or ( | ):  at least one is enough.
	- Xor (^): not the same. same = 0 and different = 1
	- Left shift (<<): make bigger, multiply by 2 per shift.
	- Right shift (>>): make smaller, divide by 2 per shift.

```python
# Example 1 = Compliment (~)
print(~12) = -13 
# Basically adds one to the number and then turns it into negative

# Example 2 = And (&)
print(10&7)
'''
10 = 1010
07 = 0111 
AND = 0010 = 2
'''

# Example 3 = OR (|)
print(10|7)
'''
10 = 1010
07 = 0111
OR = 1111 = 15
'''

# Example 4 = XOR (^)
print(10^7)
'''
10 = 1010
     ^^^^
07 = 0111
XOR= 1101 = 13
'''

# Example 4 = Left shift (<<)
print(10<<7) = # Multiply 10 by 2 (7 times) or simply 2 to the power of 7
'''
10 x 2 x 2 x 2 x 2 x 2 x 2 x 2 = 128 x 10 = 1280
1280 = 10100000000
'''

# Example 5 = Right shift (>>)
print(10>>2) = # Divide 10 by 2 (2 times)
'''
10 / 2 = 5 / 2 = 2 (no decimals)
2 = 10
'''
```

- If you work in Cryptography, this is a must!
### 6. Special Operators:
- In python, 'special operators' usually means two small groups of operators that don't do math or logic, but answer special questions about objects:
1. **Identity operators** -> check if two things are the same object; `is, is not`.
2. **Membership operators** -> check if something is inside something else; `in, not in`.
## Indentations
- Are just a white space which python uses for some of its function. If there is no proper indentation, then you are doomed with the *indentation error*.
## If-else conditions
- In computer programming, we use the if statement to run a block code only when a condition is **True**.
- For example: assigning grades (A, B and C) based on marks obtained by a student.
1. if the percentage is above 90%, assign grade A
2. if the percentage is above 75%, assign grade B
3. if the percentage is above 65%, assign grade C
- In python, there are three forms of the `if... else` statement
1. **if statement**: This statement evaluates condition.
2. **if... else statement**: an if statement can have an optional else clause.
3. **if... elif... else statement**: an if statement can have more than one optional elif clause.
### Nested if statements
- We can also use an if statement inside of an if statement. This is known as a nested if statement.

```python
number = 5

# outer if statement
if (number >= 0):
	# inner if statement
	if number == 0:
		print('Number is 0')
	# inner else statement
	else:
		print('Number is positive')
# outer else statement
else:
	print('Number is negative')
# output = Number is positve.
```

- This is an example of a simple CLI calculator, with all the concepts above:

```python
# code for a simple calculator
# This example includes some good use of if..elif..else statements and can be a good beginner example.
num1 = float(input('enter your first number: '))
num2 = float(input('enter your second number: '))

operation = int(input('which operation would you like to do?\n'
				"1. Addition\n"
				"2. Subtraction\n"
				"3. Multiplication\n"
				"4. Division\n"
				"choose(1/2/3/4): "))

if operation == 1:
	solution = num1 + num2
	print(f'Your solution is {solution}')
elif operation == 2:
	solution = num1 - num2
	print(f'Your solution is {solution}')
elif operation == 3:
	solution = num1 * num2
	print(f'Your solution is {solution}')
elif operation == 4:
	if num2 == 0:
		print("Numbers can't be divided by zero")
	else:
		solution = num1 / num2
		print(f'Your solution is {solution}')
else;
	print('only choose from 1 to 4')
```

## Logical Errors
- Errors that occur at runtime (after passing the syntax test) are called exceptions or logical errors.
- For instance, they occur when we:
	- try to call an index that is greater than the list have causes (**IndexError**)
	- try to divide a number by zero (**ZeroDivisionError**)
	- When you have error on your syntax (**NameError**) and so on.
- So, specially when errors occur on runtime this causes a huge damage on our program so we have to handle it.
- For handling errors, we use `try... except` blocks.

```python
try:
	# code that may cause exception
except:
	# code to run when exception occurs
```
-> Example 1:
```python
try:
	numerator = 10
	denominator = 0
	
	result = numerator/denominator
	
	print(result)
except:
	print("Error: Denominator cannot be 0.")
	
# output: Error: Denominator cannot be 0.
```
-> Example 2:
```python
try:

	even_numbers = [2,4,6,8]
	print(even_numbers[5])
	
except ZeroDivisionError:
	print("Denominator cannot be 0")
	
except IndexError:
	print("Index out of bound.")

# output: Index out of bound.
```
## Python Loops
- In computer programming, loops are used to **repeat a block of code**.
-> For example, if you want to show a message 100 times, then we can use a loop and print(100), this is just a simple example, you can achieve much more with loops.
- There are 2 types of loops:
	- For loop and
	- While loop.

### 1. For loop
- In python, the for loop is used to run a block of code for a certain number of times. It is used to **iterate over any sequences** such as list, tuple, string, etc.
- This kind of loop will continue for n times.
Syntax:
```python
for val in sequence:
	# statement(s)
# Sequence = can be a list, tuple, string or a range.
# val = is a variable which will hold the iteration from the sequence or holds the items or variables in the sequence.

# simple example:
for x in range(1, 11):
	print(x)
# output = lists the numbers from 1 to 10 wihtout including 11.

# anothwe example with a list:
languages = ['Python', 'JS', 'Ruby', 'Go']
for lang in languages:
	print(lang)
# output = prints out all the languages in the list.
```

#### some keywords
1. **range keyword /range(size)/** = a range is series of values between two numeric intervals. when you enter 5 in range, it prints out from 0-4.

```python
# example 1
number = range(5)
print(number)
# output: range(0, 5)

# example 2
for i in range(5)
	print(i)
# output = lists from 0 to 4
```

2. **len keyword /len(list)/** = a len is used to show the length of a sequence may be list, tuple or staffing.

```python
# example 1
a = [1, 2, 3, 4, 5, 'hello']
print(len(a))
# output = 4

# example 2
a = [1, 2, 3, 4, 5, 'hello']

for i in range(len(a)):
	print(i)
# output = prints out all the numbers except the 'hello'.
```

### 2. While loops
- These loops will continue working as long as a condition is met. We can repeat a block of code as long as a condition remains 'True'. we re-check the condition at the end of the loop.
- Syntax:

```python
while condition:
    # body of while loop

# program to display numbers from 1 to 5

# initialize the variable 
i = 1
n = 5

# while loop from i = 1 to 5
while i <= n:
    print(i)
    i = i + 1
```

**Difference between for and while**:
- Simply the for loop repeats for a fixed number of times.
- Simply the while loops repeats as long as the written condition is met.
- Example:
	- If you have a case that wanted to check level of a user and displays "You have passed {n}th level" n is sequence. Until the user level and the class level is equal. What do u do?

```python
current_level = 0
final_level = 5
while current_level <= final_level:
	print('You have passed level', current_level)
	current_level += 1
	print('Level ends')
```

- For loops: ends when the **iterable** is finished.
- While loops: ends when the condition is false.
- **Break**: used to exit from an infinite loops

```python
code = [2313, 2314, 4325, 6546]
errors = 0

while True:
	if errors <= 5:
		user = int(input(f"Enter the captcha correctly {code[0]}:\n>>"))
		if user != int(code[0]):
			print(int(code[0]))
			print(f'trail{errors}: incorrect!, try again')
			errors += 1
		elif user == int(code[0]):
			print("WellDone!")
			break
	else:
		print("try again, next time!")
		break
```
