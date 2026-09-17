# Functions in python
- A function is a block of code that performs a specific task.
- Suppose, you need to create a program to create a blue circle. You can create two functions to solve this problem:
1. A function that create a circle function
2. A function that create a color function
- Dividing a complex problem into smaller chunks makes our program easy to understand and reuse.
## Types of functions
- There are 2 types of function in python programming:
1. **Standard library functions** - These are built-in functions in python that are available to use. Almost all keywords in python are functions like *print(), len(), input()...*
2. **User-defined functions** - We can create our own functions based on our requirements.
## Creating functions
- Syntax:
```python
def function_name(arguments):
	# function body
# it has body like conditional statements.
```
-> Example 1:
```python
def greet():
	print('Hello world!')
greet()
```
- Functions have to be called to word. Think of functions like some skilled person, plumbers can do water pipe problems, their specific task is fixing broken pipes. So, If I need to fix my water pipe, what do I do? Just call the plumber! He will fix your problems.
- So in the same sense, functions have to be called.
-> Example 2
```python

-> We Have 2 functions which are called 'gtst' and 'nathan', both of these functions do different tasks.
-> When we called their name, both will print out a different output.

def gtst():
	print("learn.")
	print("DO exercise.")
	print("learn")
	
def nathan():
	print("Teach.")
	print("Answer Questions.")
	print("Prepare modules.")
	
gtst()
nathan()
```
## Function arguments
- They are used to take value while calling and insert it inside the function.

-> Example 1:
```python
# function with two arguments
def add_numbers(num1, num2):
	sum = num1 + num2
	print('Sum: ',sum)

# function call with two values
add_number(5, 4)

# Output = sum: 9
```
-> Example 2:
```python
def users(fname, lname):
	print(f"Hello {fname}!, your father name is: {lname}")

users('Nathan','Hailu')
# output: Hello Nathan!, your father name is: Hailu
```
## Return statement
- A python function may or may not return a value
- If we want our function to return some value to a function call, we use the 'return' statement.

-> Example 1
```python
def add(number1, number2):
	return number1+number2
	
add(2,3)
# output = nothing ...

def add(number1, number2):
	return number1+number2
	
print(add(2,3))
```
- As we seen before, everything are functions in python
	- so `print()` is also a function as `input(), len()`, everything!
-> Example 1:
```python
# when we do:
print('hello')
# We are calling the function and giving it an argument.
```
-> Example 2:
```python
# We can give default values too
def display(number1=100):
	print(f"the value u entered is: {number1}")
display()
# output: 100
```
## Recursion
- Recursion is the process of defining something in terms of itself. In Python, we know that a function can call other functions. 
- It is even possible for the function to call itself. These types of construct are termed as recursive functions.
-> Example 1:
```python
def factorial(x):
	"""This is a recursive function
	to find the factorial of an integer"""

	if x == 1:
		return 1
	else:
		return (x * factorial(x-1))

num = 3
print("The factorial of", num, "is", factorial(num))
```

### Advantages of Recursion
1. Recursive functions make the code look clean and elegant
2. A complex task can be broken down into simpler sub-problems using recursion
3. Sequence generation is easier with recursion than using some nested iteration

### Disadvantages of Recursion
1. Sometimes the logic behind recursionis hard to follow through
2. Recursive calls are expensive (inefficient) as they take up a lot of memory and time
3. Recursive functions are hard to debug.

## Anonymous / lambda function
- If a function doesn't have a name it is called lambda function / Anonymous.
- If you have 1 line of code to return, you don't need to **def** a function.
- A lambda function is a special type of function without the function name.
- Syntax: `lambda arguements(s) : expression`
- We use lambda keyword instead of def.

-> Example 1:
```python
# without lambda
def greet():
    return "Hello world"

print(greet())

# with lambda
greet = lambda : print('Hello World')
greet()
```

## Function takers function
### Filter function
- Filter, map & reduce takes a function as an arguement.
- Filters are used to filter or search some function from sequences.
```python
def is_even (n):
    return n%2==0

nums = [3,2,6,8,4,6,2,91]

evens = list(filter(is_even, nums))

print(evens)
```
