# Introduction

## What does a computer do?

- Perform calculations
- Remember results

## What kinds of calculations a computer do?

- Built-in to the language
- And the ones you define as a programmer

## Are simple calculations enough?

- No, we still need to think carefully about how to implement optimum solutions. Otherwise, our computers will take too much time to resolve complex problems

## But what if we just store all the pre-calculated solutions?

- That's impossible, for example, Chess has around 10^123 possible games and there are approximately 10^80 atoms in the observable universe.
- We can't just use brute-force or pre-compute, we need to be clever about how we come up with a solution

Despite its speed and size, a computer does have limitations
◦ Some problems still too complex
◦ Accurate weather prediction at a local scale
◦ Cracking encryption schemes

# Types of Knowledge

There are two types of knowledge:

- **Declarative knowledge**: They are facts, for example: "There are 25 chairs at this room". Nevertheless, here we don't know how we got to this statement.
- **Imperative knowledge**: It's about "how-to". A recipe to get to a possible solution. So instead of just saying: "There are 25 chairs at this room" we come up with a series of steps to determine the exact amount of chairs in the room. For example:
  - Take 1 chair.
  - Count 1
  - Take another chair that hasn't been taken yet
  - Add 1 to your previous number
  - Repeat until there are no more chairs left to be counted.

These series of steps (or "recipe") is what we call in computer science an **Algorithm**.

_A bit more formally, an algorithm is a finite list of instructions that describe a computation that when executed on a set of inputs will proceed through a set of well-defined states and eventually produce an output._

# Machines

There are two types of machines to process algorithms:

- Fixed program Computers
- Stored program Computers

## Fixed Program computers

They just do very specific things and nothing else. Exampĺe:

- Alan Turing's bombe machine
- A simple handled calculator

## Stored Program computer:

This machine can store and execute instructions by creating/using an instruction-set architecture.

## Basic Machine Architecture

![image](https://user-images.githubusercontent.com/1868409/67008923-e94c7580-f0c0-11e9-8c94-5ec2376eb03e.png)

- Memory and data are stored in Memory
- ALU contains the set of primitives we use to perform any calculation
- The CU is a program counter that points to a location in memory (data or instruction)
- The interpreter is another program whose responsibility is to select which instruction is executed at any moment.
- Most often, the interpreter simply goes to the next instruction in the sequence, but not always. In some cases, it performs a test, and on the basis of that test, execution may jump to some other point in the sequence of instructions. This is called: **flow of control**.

## Basic Primitives

- Turing showed you can compute anything using 6 primitives.
- Modern programming languages have a more convenient set of primitives than can abstract to create new ones.

## Turing Completeness

- A programming language is said to be Turing complete if it can be used to
  simulate a universal Turing Machine.
- All modern programming languages are Turing complete. As a consequence, anything that can be programmed in one programming language (e.g., Python) can be programmed in any other pro- gramming language (e.g., Java).

# Languages

## Aspects of a Language

Each programming language has:

- a set of primitive constructs
- a syntax
- a static semantics
- and a semantics.

## Primitive constructs

- In programming, they are numbers, strings and simple operators.
- Think of them as the words used in any spoken language.

## The Syntax

- Defines which strings of characters and symbols are well formed
- Example:
  - `3.2*5` Syntactically valid because it meets the criteria `<value> <operator> <value>`
  - `3.2 3.2` Syntactically incorrect. Doesn't meet the past criteria.
- Errors are common and easily caught

## The Static Semantics

- Defines which syntactically valid strings have a meaning
- Example:
  - `3.2 * 5`: It's sintactically correct and has a meaning.
  - `3.2 / "hi"`: It's sintactically correct but does not have a meaning. Can you divide a number between a word? I don't think so.
- Static semantic error can produce unexpected behaviors. Nevertheless, some languages check for these before running the program

## The Semantics

- It associates a meaning with each syntactically correct string of symbols that has no static semantic errors
- In spoken language the semantics might be ambiguos but in programming language. The meaning is only one. Unfortunately, this meaning is not always the intended.
- Semantic errors are usually refered as Bugs. They can have different effects:
  - Program crashes, stops running
  - Program runs forever
  - Program gives an answer but different than expected (this is the worst scenario)

# Types

## Python Programms

- A Python program, sometimes called a script, is a sequence of definitions and commands.
- The commands (or statements) are executed by the Python interpreter in something called the shell.

### Commands

- A command, often called a statement, instructs the interpreter to do something.
- For example, the statement: `print('Yankees rule!')` instructs the interpreter
  to call the function print , which will output the string "Yankees rule!" to the win-
  dow associated with the shell.

## Objects

- Objects are the core things that Python programs manipulate.
- Every object has a type that defines the kinds of things that programs can do with that object.

### Type of Objects

- **Scalar**: cannot be subdivided.
- **Non-scalar**: have internal structure that can be accessed.

## Scalar objects.

- There are four type of scalar objects:
  - **int**: represent integers, ex. 5
  - **float**: represent real numbers, ex. 3.27
  - **bool**: represent Boolean values `True` and `False`
  - **NoneType**: special and has one value, None
- You can use `type()` to see the type of an object

### Casting scalar objects

- Yout can convert object of one type to another. Example:
  - `float(3)` converts integer 3 to float 3.0
  - `int(3.9)` truncates float 3.9 to integer 3

## Expressions and Operators

- An expression is a combination of objects and operators.
- An expression has a value, which has a type

### Operations on Ints and Floats

- Some common operations:
  - `i+j`: the sum
  - `i-j`: the difference
  - `i*j`: the product
  - `i/j`: division
  - `i//j`: int division
  - `i%j`: the remainder when i is divided by j
  - `i**j`: i to the power of j
- Sum, difference, product, division and power are of type **int** if both values are int, and float if one of the values is float
- The operations int division and remainder are always float.

### Operators Precedence

- You can use parentheses to force the operators precedence. Example:
  - `3*5+1` evaluates to 16
  - `3*(5+1)` evaluates to 18
- Otherwise, you have to rely on the following default precedence:
  1. `**`
  2. `*`
  3. `/`
  4. `+` and `-` executed from left to right.

# Variables and Values
**Variables** provide a way to associate names with objects:

```
pi = 3
radius = 11
area = pi * (radius**2)
radius = 14
```
This is what happens:
![image](https://user-images.githubusercontent.com/1868409/67391140-6752c580-f574-11e9-9287-f2afc5389fb9.png)


- If the program then executes radius = 14, the name radius is rebound to a
different object of type int, as shown in the right panel of the figure above.
- Note that this assignment has no effect on the value to which area is bound. It is still bound to the object denoted by the expression 3*(11**2).

## Multiple Assignment

- Python allows multiple assignment. Example:
    - `x, y = 2, 3`
- The past assignment expression binds x to 2 and y to 3.
- This is convenient since it allows you to use multiple assignment to swap the bindings of two variables. Example:

```
x, y = 2, 3
x, y = y, x
print('x =', x)
print('y =', y)
````
- The past chunk of code will print: 
```
x = 3
y = 2
```

## Comparison and Logic operators
- `i>j`
- `i>=j`
- `i<j`
- `i<=j`
- `i==j`: **equality** test, `True` if `i` equals `j`
- `i!=j`: **inequality** test, `True` if `i` not equal to `j`
- `not a`: `True` if a is `False`, `False` if a is `True`
- `a and b`: `True` if both are `True`
- `a or b`: `True` if either or both are `True`

## Branching Programs

- The kinds of computations we have been looking at thus far are called straightline
programs. They execute one statement after another in the order in which
they appear, and stop when they run out of statements.
- Branching programs are more interesting. The simplest branching statement is a conditional. As shown next:

```
if <Boolean expression>:
    <block of code>
else:
    <block of code>
```
- This is a real example:
```
if x%2 == 0:
    print('Even')
else:
    print('Odd')
print('Done with conditional')
```
- Indentation is semantically meaningful in Python. For example, if the last statement in the above code were indented it would be part of the block of code

## Constant-time programs

- A straight-line program, that has n lines of code, will take n units of time to run.
- A branching program with *n* lines of code might take less than *n* units of time to run, but it cannot take more, since each line of code is executed at most once.
- A program for which the maximum running time is bounded by the length
of the program is said to run in constant time. It means that there exists a constant, *k*, such that the program is guaranteed to take no more than *k* steps to run. This implies that the running time does not grow with the size of the input to the program.
- Constant-time programs are quite limited in what they can do. Consider, for example, writing a program to tally the votes in an election. It would be truly surprising if one could write a program that could do this in a time that was independent of the number of votes cast. In fact, one can prove that it is impossible to do so.
- The study of the intrinsic difficulty of problems is the topic of **computational complexity**.