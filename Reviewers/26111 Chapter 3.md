---
tags: fc, plang
course: 26111 Programming Languages
---
the form or structure of the expressions, statements, and program units ;; Syntax

the meaning of the expressions, statements, and program units ;; Semantics

It is a set of sentences ;; Language

Lowest level syntactic unit of language (e.g., x, sum, begin) ;; Lexeme

category of lexemes ;; Token

A recognition device reads input strings over the alphabet of the language and decides whether the input strings belong to the language (e.g., syntax analysis part of a compiler) ;; Recognizer

A device that generates sentences of a language. We can determine if syntax of a particular sentence is correct by comparing to it. ;; Generator

Invented by John Backus to describe Algol 58. It is equivalent to context-free grammars. ;; Backus-Naur Form

It refers to the lexemes or tokens. It is a constant in BNF. ;; Terminal

It refers to the productions in BNF. ;; Non-terminal

a repeated application of rules, starting with the start symbol and ending with a sentence (all terminal symbols) ;; Derivation

Every string of symbols in a derivation ;; Sentenial Form

sentential form that has only terminal symbols ;; Sentence

A grammar is ==ambiguous== if and only if it generates a sentential form that has two or more distinct parse trees

A hierarchical representation of a derivation. ;; Parse Tree

In Extended BNF, Optional parts (0 or one) are placed in ==brackets==

In Extended BNF, Alternative parts are placed inside (1) and separated via ______(2). ;; Parenthesis, Vertical Bars

In Extended BNF, Repetitions (0 or more) are placed inside ==braces==

semantics rules that can be checked compile time (i.e., prior to runtime). As an example, variables in a program must be "declared" before they are referenced. ;; Static Semantics

semantic rules apply during the execution of a program. ;; Dynamic Semantics

It have additions to CFGs to carry some semantic info on parse tree nodes ;; Attribute Grammar

In attribute grammar, For each ______ (1) x there is a set A(x) of  (2) ;; Grammar Symbol, Attribute Values

In attribute grammar, Each rule has a set of ==functions== that define certain attributes of the non-terminals in the rule

In attribute grammar, Each rule has a (possible empty) set of ==predicates== to check for an attribute consistency

Describe the meaning of a program by executing its statements on a machine, either simulated or actual. ;; Operation Semantics

To use operational semantics for a high-level language, a ==virtual machine== is needed.

It is based on recursive function theory, and it was developed by Scott and Strachey. It is the most abstract semantics description method ;; Denotational Semantics

