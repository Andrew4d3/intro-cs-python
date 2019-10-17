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
- **Imperative knowledge**: It's about "how-to". A recipe to get to a possible solution. So instead of just saying:  "There are 25 chairs at this room" we come up with a series of steps to determine the exact amount of chairs in the room.  For example: 
    - Take 1 chair.
    - Count 1
    - Take another chair that hasn't been taken yet
    - Add 1 to your previous number
    - Repeat until there are no more chairs left to be counted.

These series of steps (or "recipe") is what we call in computer science an **Algorithm**.

*A bit more formally, an algorithm is a finite list of instructions that describe a computation that when executed on a set of inputs will proceed through a set of well-defined states and eventually produce an output.*

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

