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
