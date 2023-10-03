---
tags: fc, plang
course: 26111 Programming Languages
---

# Programming Domains

5 types of programming applications
,,
1. scientific applications
2. business applications
3. artificial intelligence
4. systems programming
5. web software

# Language evaluation criteria

5 elements of the criteria
,,
1. Readability
2. Writability
3. Reliability
4. Costs
5. Others

the ease with which programs can be read and understood ;; readability

the ease with which a language can be used to create programs in the program domain (e.g. click and drag feature) ;; writability

if a program performs to its specifications under all conditions (e.g. type checking, exception handling, etc.)

The ease with which programs can be moved from one platform to another ;; portability

The applicability to a wide range of applications ;; generality

The completeness and precision of the language's official definition ;; well-definedness

# Influences on language design

influences on language design
,,
- computer architecture
- programming methodologies

## von Neumann architecture

fetch-execute-cycle
,,
```
initialize the program counter
repeat forever
	fetch the instruction pointed by the counter
	increment the counter
	decode the instruction
	execute the instruction
	store the result
end repeat
```

when program instructions can be executed much faster than the speed of the connection between a computer's memory and its processor ;; von Neumann bottleneck

the von neumann machine is the basis of ==imperative langauges==

# Language categories

four main programming language categories
,,
- imperative
- functional
- logic
- object oriented

a subcategory of imperative languages that include drag-and-drop generation of code segments ;; visual languages

visual languages were once called ==fourth-generation languages==

a newly emerged category of languages that are not really programming languages ;; markup/programming hybrid languages

# Implementation methods

programs in a programming language are translated into machien language which can be executed directly on the computer ;; compiler implementation

the language that a compiler translates ;; source language

programs are interpreted by another program called an interpreter, with no translation whatever ;; pure interpretation implementation

this implementation translates high-level language programs to an intermediate language designed to allow easy interpretation ;; hybrid implementation systems

## Compiler implementation

the ==lexical analyzer== gathers the characters of the source proram into ==lexical units==

identifiers, special words, operators, and punctuation symbols ;; lexical units

the ==syntax analyzer== takes the lexical units from the lexical analyzer to construct ==parse trees==

hierarchical structures that represent the syntactic structure of the pogram ;; parse trees

this produces a program in a different language; at an intermediate level between the source program and the machine language program ;; intermediate code generator

intermediate langauges sometimes look very much like ==assembly languages==, and in fact, sometimes are actually it.

the user and system code after being linked together ;; load module/executable image

prc=ocess of collecting system programs and linking them to user programs ;; linking and loading/linking

a systems program that does the linking and loading ;; linker

a program that processes a program immediately before the program is compiled ;; preprocessors

## Pure interpretation

the interpreter program acts as a ==software simulation== of a machine whose ==fetch-execute== cycle deals with high-level language program statements rather than machine instructions

all ==run-time error== messages in this implementation can refer to source-level units

The bottleneck of a pure interpreter ;; statement decoding

## Hybrid implementation systems

Flow of source code
,,
- << source program
- lexical analyzer << lexical units
- lexical units >> syntax analyzer << parse trees
- parse trees >> intermediate code generator << intermediate code
- intermediate code >> interpreter << results

## Preprocessors

preprocessor instructions are commonly used to specify that the ==code from another file== is to be included.

# Programming environments

a programming environment is the ==collection of tools== used in the development of software

collection of tools in a programming environment:
,,
- file system
- a text editor
- linker
- compiler
<br> or it may include a large collection of integrated tools, each accessed through a uniform user interface.