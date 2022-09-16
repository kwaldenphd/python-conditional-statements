# Key Concepts

Specific code commands that show up in this lab:

Comparison operators:

<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>Addition</td><td><code>+</code><td><code>5 + 6</code></td><td>Adds values</td></tr>
  <tr><td>Subtraction</td><td><code>-</code><td><code>5 - 6</code></td><td>Subtracts values</td></tr>
  <tr><td>Multiplication</td><td><code>*</code><td><code>5 * 6</code></td><td>Multiples values</td></tr>
  <tr><td>Integer division</td><td><code>//</code><td><code>5 // 6</code></td><td>Divides values, integers (whole numbers)</td></tr> 
  <tr><td>Float division</td><td><code>/</code><td><code>5 / 6</code></td><td>Divides values, floating point numbers (decimal values)</td></tr>
  <tr><td>Modulo</td><td><code>%</code><td><code>5 % 6</code></td><td>Returns or retrieves remainder (whole number) from division operation</td></tr>  
  <tr><td>Exponent</td><td><code>**</code><td><code>5 ** 6</code></td><td>Calculates exponent</td></tr>
  </table>
  
Conditional statements:

<table><tr><th>Name</th><th>Syntax</th><th>Example</th></tr>
  <tr><td>If</td><td><code>if</code><td><code>if x > y</code></td></tr>
  <tr><td>Else</td><td><code>else</code><td><code>else:</code></td></tr>
  <tr><td>Else-If, Elif</td><td><code>elif</code><td><code>elif x < y:</code></td></tr>
  <tr><td>While</td><td><code>while</code><td><code>while x > y</code></td></tr> 
  </table>

## Boolean Logic
- "In mathematics and mathematical logic, Boolean algebra is the branch of algebra in which the values of the variables are the truth values true and false, usually denoted 1 and 0" ([Wikipedia](https://en.wikipedia.org/wiki/Boolean_algebra))
- "You can evaluate any expression in Python, and get one of two answers, `True` or `False`. When you compare two values, the expression is evaluated and Python returns the Boolean answer" ([W3Schools, Python Booleans](https://www.w3schools.com/python/python_booleans.asp))

Python example:

```Python
print(4 == 5) # returns false
print(6 < 10) # returns true

# boolean logic with variables
x = 5
y = 6
print(x > y) # returns false
```

## Comparison Operators (or relational operators)

- "The relational operators are often used to create a test expression that controls program flow. This type of expression is also known as a Boolean expression because they create a Boolean answer or value when evaluated. There are six common relational operators that give a Boolean value by comparing (showing the relationship) between two operands. If the operands are of different data types, implicit promotion occurs to convert the operands to the same data type" (Busbee, "[Relational Operators](https://press.rebus.community/programmingfundamentals/chapter/relational-operators/)")

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

**Complex Conditional Statements**
- Conditional statements that compare more than two values or evaluate multiple comparisons as part of a conditional statement.

Python examples:

```Python
# an example that compares three integers
print(5 < 6 > 7) # returns false because 6 is not greater than 7

# an example that compares three strings
print("apple" > "banana" < "blueberry") # returns false because apple comes before or is less than banana
```

We can also compare or relate multiple conditions using logical operators: `and`, `or`, `not`

```Python
# example using logical operators
print(5 < 6 and 6 < 7) # returns true because both statements are true

print(5 < 6 or 6 > 7) # returns true because at least one statement is true

print(not(5 < 6 and 6 < 7)) # returns false, inverse of initial true
```

**Control Structures**

From Busbee and Braunschweig's "[Structured Programming](https://press.rebus.community/programmingfundamentals/chapter/structured-programming/)" from *Programming Fundamentals*
    
"One of the most important concepts of programming is the ability to control a program so that different lines of code are executed or that some lines of code are executed many times. The mechanisms that allow us to control the flow of execution are called control structures. Flowcharting is a method of documenting (charting) the flow (or paths) that a program would execute. There are three main categories of control structures:"
  * Sequence [executes in given sequence]
  * Selection [selects between two or more flows using condition or question]
  * Iteration [repeats same piece of code multiple times]
    
Examples of control structures in Python include:
- `if-then-else` (syntax: `if`, `else`, `elif`)
- `while` statements (syntax: `while`)

## `If-Then-Else`

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

Another way to express this program's logic is using `while`:
    
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
For more on `if-then-else` logic in Python:
- [W3Schools, Python If ... Else](https://www.w3schools.com/python/python_conditions.asp)

## Logical Operators
- "A logical operator is a symbol or word used to connect two or more expressions such that the value of the compound expression produced depends only on that of the original expressions and on the meaning of the operator. Common logical operators include AND, OR, and NOT." (Busbee and Braunschweig, "[Logical Operators](https://press.rebus.community/programmingfundamentals/chapter/logical-operators/)")

Logical operators in Python:
    
<table><tr><th>Name</th><th>Syntax</th><th>Example</th><th>Description</th></tr>
  <tr><td>And</td><td><code>and</code><td><code>x == y and y != z</code></td><td>Returns <code>True</code> if both statements are true</td></tr>
  <tr><td>Or</td><td><code>or</code><td><code>x != y or y == z</code></td><td>Returns <code>True</code> if one of the statements is true</td></tr>
  <tr><td>Not</td><td><code>not</code><td><code>not(x == y and y != z)</code></td><td>Reverses the result, returns <code>False</code> if the result is true</td></tr>
  </table>
    
For more on logical operators in Python: [W3Schools, Python Logical Operators](https://www.w3schools.com/python/gloss_python_logical_operators.asp)    
