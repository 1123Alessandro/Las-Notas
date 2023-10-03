#fc #plang 

the form or structure of the expressions, statements, and program units;;Syntax

the meaning of the expressions, statements, and program units;;Semantics

It is a set of sentences;;Language

Lowest level syntactic unit of language (e.g., x, sum, begin) ;; Lexeme

category of lexemes ;; Token

A recognition device reads input strings over the alphabet of the language and decides whether the input strings belong to the language (e.g., syntax analysis part of a compiler) ;; Recognizer

A device that generates sentences of a language. We can determine if syntax of a particular sentence is correct by comparing to it.;;Generator

Invented by John Backus to describe Algol 58. It is equivalent to context-free grammars.;;Backus-Naur Form

It refers to the lexemes or tokens. It is a constant in BNF.;;Terminal

It refers to the productions in BNF.;;Non-terminal

a repeated application of rules, starting with the start symbol and ending with a sentence (all terminal symbols);;Derivation

Every string of symbols in a derivation;;Sentenial Form

sentential form that has only terminal symbols;;Sentence

A grammar is ________ if and only if it generates a sentential form that has two or more distinct parse trees;;Ambiguous

A hierarchical representation of a derivation.;;Parse Tree

In Extended BNF, Optional parts (0 or one) are placed in ______;;Brackets

In Extended BNF, Alternative parts are placed inside (1) and separated via ______(2).;;Parenthesis, Vertical Bars

In Extended BNF, Repetitions (0 or more) are placed inside ______;;Braces

semantics rules that can be checked compile time (i.e., prior to runtime). As an example, variables in a program must be "declared" before they are referenced.;;Static Semantics

semantic rules apply during the execution of a program.;;Dynamic Semantics

It have additions to CFGs to carry some semantic info on parse tree nodes;;Attribute Grammar

In attribute grammar, For each ______ (1) x there is a set A(x) of  (2);;Grammar Symbol, Attribute Values

In attribute grammar, Each rule has a set of _______ that define certain attributes of the non-terminals in the rule;;Functions

In attribute grammar, Each rule has a (possible empty) set of _________ to check for an attribute consistency;;Predicates

Describe the meaning of a program by executing its statements on a machine, either simulated or actual.;;Operation Semantics

To use operational semantics for a high-level language, a ________ is needed.;;Virtual Machine

It is based on recursive function theory, and it was developed by Scott and Strachey. It is the most abstract semantics description method;;Denotational Semantics


Three ways to Implement Programming Languages;;Compilation, Pure interpretation, and Hybrid implementation

What analyzer does Compilation, Pure interpretation, and Hybrid implementation use;;Lexical and Syntax Analyzer

Deals with small-scale language constructs, such as names and numeric literals.;;Lexical Analyzer

Deals with large-scale constructs, such as expressions, statements, and program units.;;Syntax Analyzer

Why do the compilers separate the analyzers?;;Simplicity, Efficiency, and Portability

Removes the details of lexical analysis from the syntax analyzer which makes it smaller and less complex;;Simplicity

It becomes easier to optimize the lexical analyzer.;;Efficiency

The lexical analyzer reads source files, so it may be platform-dependent;;Portability

collects input characters into groups (lexemes) and assigns an internal code (a token) to each group;;A lexical analyzer collects

are recognized by matching the input against patterns.;;Lexemes

are usually coded as integer values, but for the sake of readability, theyare often referenced through named constants;;Tokens

Directed Graph (it recognizes names, integer literals, parentheses, and arithmetic operators);;State Diagram

The nodes are labeled with state names.  
The arcs are labeled with input characters.  
An arc may also include actions to be done when the transition is taken;;State Diagram have:

Gets the next input character and puts it in a global variable namednextChar. Also determines the character class of the input character andputs it in the global variable charClass.;;getChar

Adds the character in nextChar to the end of lexeme.;;addChar

Skips white space;;getNonBlank

Computes the token code for single-character tokens (parentheses and arithmetic operators).;;lookup

Often reffered to as Syntax Analysis;;Parsing

Determine whether the input program is syntactically correct.Produce a parse tree.;;Responsibilities of a syntax analyzer, or parser

Parsers are categorized by;;Top Down Bottom up

Parsers build the tree from the root downward to the leaves.;;Top-down

Parsers build the tree from the leaves upward to the root.;;Bottom-up

Lowercase letters at the beginning of the alphabet (a, b, ...);;Terminal symbols

Uppercase letters at the beginning of the alphabet (A, B;;Nonterminal symbols

Uppercase letters at the end of the alphabet (W, X,Y, Z);;Terminals or nonterminals

Lowercase letters at the end of the alphabet (w, x, y, z);;Strings of terminals

Lowercase Greek letters (α, β,γ, δ);;Mixed strings (terminals and/or nonterminals)

is coded directly from the BNF description of the syntax of a language.An alternative is to use a parsing table rather than code.;;A recursive-descent parser

The first L in LL speci-fies a left-to-right scan of the input; the second L specifies that a leftmost deriva-tion is generated;;LL Parser

he Lspecifies a left-to-right scan and the R specifies that a rightmost derivation is generated;;LR

The correct RHS to reduce;;Handle

used to test a non-left-recursive grammar todetermine whether it can be parsed in a top-down fashion. This test requirescomputing FIRST sets;;pairwise disjointness test

a string consisting of all of the leaves of the partial parse tree that is rooted at one particular internal node of the whole parse tree.;;phrase

a phrase that is derived from a non-terminal in a single step.;;simple phrase

They can be built for all programming languages. They can detect syntax errors as soon as possible in a left-to-right scan. The LR class of grammars is a proper superset of the class parsable by LL pars-ers;;Advantages of LR parsers

Bottom-up parsers are often called;;shift-reduce algorithms

a string of characters used to identify some entity in a program;;name

uppercase and lowercase letters in names are distinct. EX. rose differs from ROSE;;case sensitive

a special word of a programming language that cannot be used as a name;;reserved word

of a variable, is the machine memory address with which it is associated;;address

address of a variable;;l-value

when more than one variable name can be used to access the same memory location, the variable name is called;;aliases

of a variable, determines the range of values the variables can store;;type

of a variable, is the contents of the memory cell or cells associated with the variable;;value

a variables value;;r-value

an association between an attribute and an entity, such as between a variable and its type or value, or between an operation and a symbol;;binding

the time at which a binding takes place;;binding time

it first occurs before run time begins and remains unchanged throughout program execution;;static binding

if the binding first occurs during run time or change in the course of program execution;;dynamic binding

a statement in a program that lists variable names and specifies that they are a particular type;;explicit declaration

a means of associating variables with types through default conventions, rather than declaration statments;;implicit declaration

a kind of type decleration that uses context;;type interference

when you bind a variable to a pool of avaliable memory;;allocation

the process of placing a memory cell that has been unbound from a variable back into the pool of avaliable memory;;deallocation

of a variable, is the time during which the variable is bound to a specific memory location;;lifetime

those that are bound to a memory cells before the program execution begins and remain bound to those same memory cells until program execution terminates;;static variables

are those whose storage bindings are created when their decleration statements are delaborated, but whose types are statically bound;;stack-dynamic variables

of such declerations, refers to the storage allocation and binding process indicated by the decleration, which takes place when execution reaches the code to which the decleration is attached;;elaboration

are nameless(abstract) memory cells that are allocated and deallocated by explicit run-time based instructions written by the programmer;;explicit heap-dynamic variables

are bound to heap storage only when they are assigned values;;implicit heap-dynamic variables

of a variable, is the range of statements in which the variable is visible;;scope

when a variable in a statement can be referenced or assigned in that statement;;visible

when a variable is declared in a program unit or block;;local

the scope of a variable can be statically determined, that is prior to execution;;static scoping

look at page 236 of the book for this reference;;static parent

look at page 236 of the book for this reference;;static ancestors

when a section of code allocate storage when the section is entered and deallocate it when the section is exited;;block

blocks provide the origin of this phrase;;block-structured language

based on the calling sequence of subprogams, not on their spatial relationship to each other;;dynamic scoping

of a statement, is the collection of all variables that are visible in the statement;;referencing environment

if a subprograms execution has begun but has not yet terminated;;active

is a variable that is bound to a value only once;;named constants
