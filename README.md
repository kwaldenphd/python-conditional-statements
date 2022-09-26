# Comparison Operators & Conditional Statements in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>This tutorial was written by Katherine Walden and is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Overview & Goals

This lab provides an overview of foundational programming concepts in the areas of control structures and conditional execution, with a focus on Python syntax. Specific topics covered include: 
- Relational or comparison operators
- Boolean logic and logical operators
- `if-then-else` logic
- `while` statements
- Complex conditional statements

## Acknowledgements

Elements of this lab procedure were adapted from materials developed by:
- [Dr. Peter Bui](http://www3.nd.edu/~pbui/) for the [CSE 10101 "Elements of Computing I" course](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/).
  * [Conditional and Alternative Execution](http://nbviewer.jupyter.org/urls/gitlab.com/snippets/25773/raw)
- [Dr. Janet Davis](https://cs.whitman.edu/~davisj/) for the the [CSC 105 "The Digital Age" course](https://www.cs.grinnell.edu/~davisjan/csc/105/2012S/). 
  * [Laboratory: Programming in Python (Decisions and Repetition)](http://www.cs.grinnell.edu/~davisjan/csc/105/labs/python3.html)
- [Dr. Corey Pennycuff](https://www3.nd.edu/~cpennycu/) for the [CSE 10101 Elements of Computing (Fall 2019)](https://www3.nd.edu/~cpennycu/2019/fa-CSE10101-CDT30010.html).
  * [Control flow structures](https://www3.nd.edu/~cpennycu/2019/assets/fall/EOC/19.09.03.ipynb)
- [Lindsay K. Mattock](http://lindsaymattock.net/) for the the [SLIS 5020 Computing Foundations course](http://lindsaymattock.net/computingfoundations.html). 

# Table of Contents
- [Key Concepts](#key-concepts)
- [Lab Notebook Template](#lab-notebook-template)
- [Overview](#overview)
- [Comparison Operators](#comparison-operators)
  * [Boolean Logic](#boolean-logic)
  * [Boolean Logic & Comparison Operators](#boolean-logic--comparison-operators)
  * [Comparison Operators & String Objects](#comparison-operators--string-objects)
- [`if-then-else`](#if-then-else)
  * [`while` Statements](#while-statements)
  * [Indentation](#indentation)
- [Putting It All Together](#putting-it-all-together)
- [How to Submit This Lab (and show your work)](#how-to-submit-this-lab-and-show-your-work)
- [Lab Notebook Questions](#lab-notebook-questions)

[Click here](https://colab.research.google.com/drive/1UYWn9aXNzacQrxIWut9VR6zqTkCwt6gx?usp=sharing) to access this lab procedure as a Jupyter Notebook.

## Key Concepts

[Click here](https://github.com/kwaldenphd/python-conditional-statements/blob/main/key-concepts.md) for a full list of key concepts and definitions from this lab.

## Lab Notebook Template

[Click here](https://replit.com/team/eoc-f22/Conditional-Statements-in-Python) to make a copy of the Replit template for this lab.

Alternatives:
- [`.py` template](https://drive.google.com/file/d/1WZSeR0PP4Vpuy6B37zBcSYxYxkMyOK-W/view?usp=sharing) (Google Drive, ND users)
- [Jupyter Notebook, `.ipynb`](https://colab.research.google.com/drive/171iknHXXUMLEO-yyUCI1g-MbRAKFgAOv?usp=sharing) (Google Colab, ND users)

## How to submit this lab (and show your work)

Moving forward, we'll submit lab notebooks as `.py` files. 

One option is to have a `.py` file that you use to run code and test programs while working through the lab. When ready to submit the lab notebook, you add comments and remove extraneous materials.

Another option is to have an "official" `.py` file that you are using as a lab notebook (separate from your working/testing file). Use comments in Python to note when you are starting a new question (as well as answering a question).
  * Example: `Lab_Notebook_Walden.py`

What gets submitted as the lab notebook is the `Lab_Notebook_Walden.py` file.
- When in doubt, use comments
- Be sure you are using comments to note what question you're responding to

# Overview

From Busbee and Braunschweig's "[Structured Programming](https://press.rebus.community/programmingfundamentals/chapter/structured-programming/)" from *Programming Fundamentals*
    
"One of the most important concepts of programming is the ability to control a program so that different lines of code are executed or that some lines of code are executed many times. The mechanisms that allow us to control the flow of execution are called control structures. Flowcharting is a method of documenting (charting) the flow (or paths) that a program would execute. There are three main categories of control structures:"
  * Sequence [executes in given sequence]
  * Selection [selects between two or more flows using condition or question]
  * Iteration [repeats same piece of code multiple times]
  
We're going to spend multiple labs thinking through control structures and control flow, with a focus on how we use them in Python.
    
Examples of control structures in Python include:
- `if-then-else` (syntax: `if`, `else`, `elif`)
- `while` statements (syntax: `while`)

Foundational to most control structures are something called conditional statements- code that tests whether a condition is `True` or `False`. 

# Comparison Operators

"The relational operators are often used to create a test expression that controls program flow. This type of expression is also known as a Boolean expression because they create a Boolean answer or value when evaluated. There are six common relational operators that give a Boolean value by comparing (showing the relationship) between two operands. If the operands are of different data types, implicit promotion occurs to convert the operands to the same data type" (Busbee, "[Relational Operators](https://press.rebus.community/programmingfundamentals/chapter/relational-operators/)", in *Programming Fundamentals*)

Relational operators, also called comparison operators, allow us to run `True/False` tests on specific conditions, focusing on the relationship(s) between two or more values.

Relational operators or comparison operators in Python: 

<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>Equal</td><td><code>==</code><td><code>x == y</code></td><td>Tests if values are equal</td></tr>
  <tr><td>Not equal</td><td><code>!=</code><td><code>x != y</code></td><td>Tests if values are not equal</td></tr>
  <tr><td>Greater than</td><td><code>></code><td><code>x > y</code></td><td>Tests is a value is greater than another</td></tr>
  <tr><td>Less than</td><td><code><</code><td><code>x < y</code></td><td>Tests is a value is less than another</td></tr> 
  <tr><td>Greater than or equal to</td><td><code>>=</code><td><code>x >= y</code></td><td>Tests if a value is greater than or equal to another</td></tr>
  <tr><td>Less than or equal to</td><td><code><=</code><td><code>x <= y</code></td><td>Tests if a value is less than or equal to another</td></tr>  
  </table>
    
For more on comparison operators in Python: [W3Schools, Python Comparison Operators](https://www.w3schools.com/python/gloss_python_comparison_operators.asp)

## Boolean Logic

- "In mathematics and mathematical logic, Boolean algebra is the branch of algebra in which the values of the variables are the truth values true and false, usually denoted 1 and 0" ([Wikipedia](https://en.wikipedia.org/wiki/Boolean_algebra))

We've talked previously about the Boolean data type. The underlying `True`/`False` logic lets us test for specific conditions and then specify how our code will execute based on the truth value for those conditional statements.

- "You can evaluate any expression in Python, and get one of two answers, `True` or `False`. When you compare two values, the expression is evaluated and Python returns the Boolean answer" ([W3Schools, Python Booleans](https://www.w3schools.com/python/python_booleans.asp))

## Boolean Logic & Comparison Operators
   
We can use comparison operators with a `print()` statement to test whether a particular statement is `True` or `False`.
   
A couple Python examples:

```Python
print(4 == 5) # returns false
print(6 < 10) # returns true
```

```Python
# comparison operator using variables
x = 5
y = 6

print(x > y) # returns false
```

## Comparison Operators & String Objects

We can probably make intuitive sense of how these comparison operators would work for numeric values. But what about text characters or string objects?
   
Most programming languages treat the 26 characters in the English-language alphabet (`a-z`) as sequential values, where `a` is less than `b`, which is less than `c`, etc.

When working with string objects that represent words or characters, comparison operators indicate positionality in the English-language alphabet.

A few examples in Python:
```
print("apple" > "banana") # returns true

print("Ohio State" > "Notre Dame") # returns false
```   

## Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSd20NlXelKfF3hS5ftvjJAPG_Db7uMbnODfIT8dGZ39fP5EaA/viewform?usp=sf_link">Comparison Operators Comprehension Check</a></td>
  </tr>
  </table>

## Application

Q1: Write a program that uses each of Python's comparison operators (`==, !=, >, <, >=, <=`) to compare two numeric values. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first numeric value

# second numeric value

# equal

# not equal

# greater than

# less than

# greater than or equal to

# less than or equal to

```

Q2: Write a program that uses each of Python's comparison operators (`==, !=, >, <, >=, <=`) to compare two string objects. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first string object

# second string object

# equal

# not equal

# greater than

# less than

# greater than or equal to

# less than or equal to

```

Q3: Write a program that asks a user to enter their age and returns an output message comparing that value with your age. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program:
```
Your age: 10

My age: 12

I am older!
```

# `if-then-else` 

From Busbee and Braunschweig's "[Selection Control Structures](https://press.rebus.community/programmingfundamentals/chapter/selection-control-structures/)" from *Programming Fundamentals*:
- "The basic attribute of a selection control structure is to be able to select between two or more alternate paths. This is described as either two-way selection or multi-way selection. A question using Boolean concepts usually controls which path is selected. All of the paths from a selection control structure join back up at the end of the control structure, before moving on to the next lines of code in a program."
- "The if then else control structure is a two-way selection"

In Python, this logic is expressed using the `if`, `else`, and `elif` syntax. From W3Schols, "[Python Conditions](https://www.w3schools.com/python/python_conditions.asp)":
- "An 'if statement' is written by using the `if` keyword"
- "The `elif` keyword is Python's way of saying 'if the previous conditions were not true, then try this condition'"
- "The `else` keyword catches anything which isn't caught by the preceding conditions"

```Python
# assign variables
x = 5
y = 7

# if statement
if x > y:
    print("The value of x is greater than the value of y")

# else if statement
elif x == y:
    print("The value of x is equal to the value of y")

# else statement
else:
    print("The value of x is less than the value of y")
```

To frame this another way:
- `if` introduces and evaluates an initial condition. The lines of code indented under `if` will only run when the `if` statement is `True`
- `else-if` or `elif` introduces and evaluates another condition. The lines of code indented under `elif` will only run when the `elif` statement is `True`
- `else` **does not** introduce a new condition. The lines of code indented under `else` will only run when the preceeding `if`/`elif` statements **are not** true 

For more on `if-then-else` logic in Python:
- [W3Schools, Python If ... Else](https://www.w3schools.com/python/python_conditions.asp)

## `while` statements

Another way to express `if-then-else` logic in Python is using a `while` statement. 

A `while` statement tests for an initial condition, and the lines of code indented under `while` run only when the initial condition is `True`.

An example of the prior `if-then-else` program, written using `while`.
    
```Python
# while statement with initial condition
while x != y:
  # if statement
  if x > y:
      print("The value of x is greater than the value of y")

      # else if statement
  elif x == y:
      print("The value of x is equal to the value of y")

  # else statement
  else:
      print("The value of x is less than the value of y")
```

As we see in this example, we can nest multiple `if-then-else` logical statements in the same piece of code.

## Indentation

As we continue to introduce more programming concepts and further our work in Python, we're starting to see **code blocks** and **indentation** at work.

From Busbee and Braunschweig's "[Code Blocks](https://press.rebus.community/programmingfundamentals/chapter/code-blocks/)" from *Programming Fundamentals*:
- "A code block, sometimes referred to as a compound statement, is a lexical structure of source code which is grouped together. Blocks consist of one or more declarations and statements. A programming language that permits the creation of blocks, including blocks nested within other blocks, is called a block-structured programming language. Blocks are fundamental to structured programming, where control structures are formed from blocks."
   
In Python syntax, code blocks are marked by indentation, or indented lines of code. 

```Python
# an example of indentation in Python
if expression:
   statement
   statement
else:
   statement
   statement
```

## Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSfP5zF_hGh2tEgr0pz3D56a6YiIkjJxcfRZq5YAHcjhZQ3wqw/viewform?usp=sf_link"><code>if-then-else</code> Comprehension Check</a></td>
  </tr>
  </table>

## Application

Q4: Write a program that asks a user to enter a color value and returns an output message comparing that value with your favorite color. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program:
```
Your favorite color: green

My age: blue

We don't have the same favorite color.
```

Q5: Modify your Q4 program to write a program that asks the user to enter a color value and returns an output message indicating whether the color is a primary, secondary, or tertiary color. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Primary colors:
- Red
- Yellow
- Blue

Secondary colors:
- Green
- Orange
- Purple

Tertiary colors:
- Amber
- Vermillion
- Magenta
- Violet
- Teal
- Chartreuse

Q6: Write a program that lets the user play a guessing game.
- First, your program should set a number as the "correct answer"
- Then, your program will ask the user to guess a number
- Your program should give a message indicating whether the user's guess is correct, too high, or too low

This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program (for a correct answer of 7:
```
You guessed 13.

This guess is too high.

Better luck next time!
```

Q7: Revise your Q6 program to use a `while` statement and continue accept new user inputs until until the user guesses the correct number.

Remember the lines of code nested under a `while` statement will continue to run (or loop) as long as the initial condition is true. The program will stop running (or looping) this code block when the initial condition is no longer true.

The general logic flow for this program:
```
1- Accept user input

2- Evaluate initial condition

3- Check if guess is too high

4- If guess is too high, output message to user and accept another guess.

5- Check if guess is too low

6- If guess is too low, output message to user and accept another guess

7- Output final message indicating user has guessed correctly
```

Note that lines 2-6 will need to continue running (or looping) until the user guesses correctly.

Answer to this question includes program + comments that document process and explain your code.

# Putting It All Together
   
We can imagine programming scenarios in which we want to compare more than two values or evaluate multiple conditions as part of a conditional statement. We can do this using logical operators and complex conditional statements.

For example, `5 < 6 > 7` evaluates whether `5` is less than `6` and `6` is greater than `7`. This statement would return `False`.

An example using strings: `"apple" > "banana" < "blueberry"` evaluates whether `"apple"` is greater than (or comes after) `"banana"` and whether `"banana"` is less than (or comes before) `"blueberry"`. This statement would return `False`.

Python examples:

```Python
# an example that compares three integers
print(5 < 6 > 7) # returns false because 6 is not greater than 7

# an example that compares three strings
print("apple" > "banana" < "blueberry") # returns false because apple comes before or is less than banana
```

We can also compare or relate multiple conditions using logical operators: `and`, `or`, `not`

- "A logical operator is a symbol or word used to connect two or more expressions such that the value of the compound expression produced depends only on that of the original expressions and on the meaning of the operator. Common logical operators include AND, OR, and NOT." (Busbee and Braunschweig, "[Logical Operators](https://press.rebus.community/programmingfundamentals/chapter/logical-operators/)")                            

For example, `5 < 6 and 6 < 7` evaluates whether `5 < 6` and `6 < 7` are true. This statement would return `True`.

Another example: `5 < 6 or 6 > 7` evaluates whether `5 < 6` or `6 > 7` is true. This statement would return `True`.

Logical operators in Python:
    
<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>And</td><td><code>and</code><td><code>x == y and y != z</code></td><td>Returns <code>True</code> if both statements are true</td></tr>
  <tr><td>Or</td><td><code>or</code><td><code>x != y or y == z</code></td><td>Returns <code>True</code> if one of the statements is true</td></tr>
  <tr><td>Not</td><td><code>not</code><td><code>not(x == y and y != z)</code></td><td>Reverses the result, returns <code>False</code> if the result is true</td></tr>
  </table>
    
```Python
# example using logical operators
print(5 < 6 and 6 < 7) # returns true because both statements are true

print(5 < 6 or 6 > 7) # returns true because at least one statement is true

print(not(5 < 6 and 6 < 7)) # returns false, inverse of initial true
```

For more on logical operators in Python: [W3Schools, Python Logical Operators](https://www.w3schools.com/python/gloss_python_logical_operators.asp)   

## Comprehension Check

<table>
 <tr><td>
<img src="https://github.com/kwaldenphd/internet/blob/main/images/clipboard.png?raw=true" alt="Clipboard icon" width="50"/></td>
  <td><a href="https://docs.google.com/forms/d/e/1FAIpQLSeLWTw1QgP8g3nrgGAUJNhgyRP9wzEo-3CcHF_YlgmiXklUyw/viewform?usp=sf_link">Logical Operators & Complex Conditional Statements Comprehension Check</a></td>
  </tr>
  </table>

## Application

Q8: Write a program that uses Python's comparison operators (`==, !=, >, <, >=, <=`) to compare at least three (3) numeric values. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first numeric value

# second numeric value

# third numeric value

# complex comparison statement

```

Q9: Write a program that uses Python's comparison operators (`==, !=, >, <, >=, <=`) to compare at least three (3) string objects. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first string object

# second string object

# third string object

# complex comparison statement

```
   
Q10: Write a program that uses Python's `and` and `or` logical operators to compare (at least) two comparison statements. Answer to this question includes program + comments that document process and explain your code.

# Lab Notebook Questions

[Click here](https://replit.com/team/eoc-f22/Conditional-Statements-in-Python) to make a copy of the Replit template for this lab.

Alternatives:
- [`.py` template](https://drive.google.com/file/d/1WZSeR0PP4Vpuy6B37zBcSYxYxkMyOK-W/view?usp=sharing) (Google Drive, ND users)
- [Jupyter Notebook, `.ipynb`](https://colab.research.google.com/drive/171iknHXXUMLEO-yyUCI1g-MbRAKFgAOv?usp=sharing) (Google Colab, ND users)

Q1: Write a program that uses each of Python's comparison operators (`==, !=, >, <, >=, <=`) to compare two numeric values. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first numeric value

# second numeric value

# equal

# not equal

# greater than

# less than

# greater than or equal to

# less than or equal to

```

Q2: Write a program that uses each of Python's comparison operators (`==, !=, >, <, >=, <=`) to compare two string objects. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first string object

# second string object

# equal

# not equal

# greater than

# less than

# greater than or equal to

# less than or equal to

```

Q3: Write a program that asks a user to enter their age and returns an output message comparing that value with your age. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program:
```
Your age: 10

My age: 12

I am older!
```

Q4: Write a program that asks a user to enter a color value and returns an output message comparing that value with your favorite color. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program:
```
Your favorite color: green

My age: blue

We don't have the same favorite color.
```

Q5: Modify your Q4 program to write a program that asks the user to enter a color value and returns an output message indicating whether the color is a primary, secondary, or tertiary color. This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Primary colors:
- Red
- Yellow
- Blue

Secondary colors:
- Green
- Orange
- Purple

Tertiary colors:
- Amber
- Vermillion
- Magenta
- Violet
- Teal
- Chartreuse

Q6: Write a program that lets the user play a guessing game.
- First, your program should set a number as the "correct answer"
- Then, your program will ask the user to guess a number
- Your program should give a message indicating whether the user's guess is correct, too high, or too low

This program will use a combination of the `input()` function, comparison operators, and `if-then-else` logic. Answer to this question includes program + comments that document process and explain your code.

Sample output for this program (for a correct answer of 7:
```
You guessed 13.

This guess is too high.

Better luck next time!
```

Q7: Revise your Q6 program to use a `while` statement and continue accept new user inputs until until the user guesses the correct number.

Remember the lines of code nested under a `while` statement will continue to run (or loop) as long as the initial condition is true. The program will stop running (or looping) this code block when the initial condition is no longer true.

The general logic flow for this program:
```
1- Accept user input

2- Evaluate initial condition

3- Check if guess is too high

4- If guess is too high, output message to user and accept another guess.

5- Check if guess is too low

6- If guess is too low, output message to user and accept another guess

7- Output final message indicating user has guessed correctly
```

Note that lines 2-6 will need to continue running (or looping) until the user guesses correctly.

Answer to this question includes program + comments that document process and explain your code.

Q8: Write a program that uses Python's comparison operators (`==, !=, >, <, >=, <=`) to compare at least three (3) numeric values. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first numeric value

# second numeric value

# third numeric value

# complex comparison statement

```

Q9: Write a program that uses Python's comparison operators (`==, !=, >, <, >=, <=`) to compare at least three (3) string objects. Answer to this question includes program + comments that document process and explain your code.

Outline for this program:
```
# first string object

# second string object

# third string object

# complex comparison statement

```
   
Q10: Write a program that uses Python's `and` and `or` logical operators to compare (at least) two comparison statements. Answer to this question includes program + comments that document process and explain your code.
