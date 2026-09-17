# What is Bash script?
- **BASH** = Bourne Again Shell
- It is a shell, that is used to interact with your kernel
- **Script** = a file that contains shell commands in a simple and clear algorithm
- The original is SH - Bourne Shell
## Uses of bash
- Script development
- Automating tasks
- Simplifying your linux ability
- Developing hacking scripts
## Starting with bash
- Bash files can have "*.sh*" extension, but you can have it without the file extension too. The files have to have executable permissions.
- You can use any text editors you want/need: basically any editor you can think of.
## Displaying output
- To start every bash script use shebang
```bash
# !/bin/bash
# !/bin/sh
```
- To display output on bash you just do:
```bash
echo "HELLO WORLD"
```
- To run your bash project, you can do it in several methods:
```bash
# !/bin/bash
# You have a project called project.sh
method 1 = /bin/bash project.sh
method 2 = ./hello.sh -> needs executable permission
method 3 = hello -> needs executable permission
```
![[bash_displaying_output.png]]
# Variables
- Bash variables are same with python variables, with some exceptions.
- Syntax:
```bash
VARIABLE_NAME="value" # no space between the equal sign
NAME = "NATHAN" #ERROR
NAME="NATHAN" # CORRECT
# Never start with numbers and use double quotes only
```
- To use the variable we will use dollar sign($) before the variable name
- If you want to display the variable sticked with other text use $[VARIABLE_NAME].
- Bash variables are string by default.
- The set command can be used to assign values to positional parameters
![[set_command_bash.png]]
## System variables
- Are variables those are declared by the system
- Here are so many: LANG, TERM, MAIL, EDITOR, USER, SHELL...
- USER displays computer owner(host)
## Variables & Data Types
- As we saw, the previous method they create strings only.
- So to create other data types we use declare.
- Arrays:
    - Arrays are lists or tuples on python
    - Syntax:
```bash
var=("list1""list2""list3""list4")
${var[0]} # To display output by using index.
${var[@]} # To display all the elements.
``` 
