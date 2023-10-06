---
tags: fc, plang
course: 26111 Programming Languages
---
a string of characters used to identify some entity in a program ;; name

uppercase and lowercase letters in names are distinct. EX. rose differs from ROSE ;; case sensitive

a special word of a programming language that cannot be used as a name ;; reserved word

of a variable, is the machine memory location with which it is associated ;; memory address

address of a variable ;; l-value

when more than one variable name can be used to access the same memory location, the variable name is called ==aliases==

of a variable, determines the range of values the variables can store ;; type

of a variable, is the contents of the memory cell or cells associated with the variable ;; value

a variables value ;; r-value

an association between an attribute and an entity, such as between a variable and its type or value, or between an operation and a symbol ;; binding

the time at which a binding takes place ;; binding time

binding that first occurs before run time begins and remains unchanged throughout program execution ;; static binding

if the binding first occurs during run time or change in the course of program execution ;; dynamic binding

a statement in a program that lists variable names and specifies that they are a particular type ;; explicit declaration

a means of associating variables with types through default conventions, rather than declaration statments ;; implicit declaration

a kind of type decleration that uses context ;; type interference

when you bind a variable to a pool of avaliable memory ;; allocation

the process of placing a memory cell that has been unbound from a variable back into the pool of avaliable memory ;; deallocation

of a variable, is the time during which the variable is bound to a specific memory location ;; lifetime

those that are bound to a memory cells before the program execution begins and remain bound to those same memory cells until program execution terminates ;; static variables

are those whose storage bindings are created when their decleration statements are elaborated, but whose types are statically bound ;; stack-dynamic variables

of such declerations, refers to the storage allocation and binding process indicated by the decleration, which takes place when execution reaches the code to which the decleration is attached ;; elaboration

==explicit heap-dynamic variables== are nameless(abstract) memory cells that are allocated and deallocated by explicit run-time based instructions written by the programmer

==implicit heap-dynamic variables== are bound to heap storage only when they are assigned values

of a variable, is the range of statements in which the variable is visible ;; scope

when a variable in a statement can be referenced or assigned in that statement ;; visible

when a variable is declared in a program unit or block ;; local

the scope of a variable can be statically determined, that is prior to execution ;; static scoping

look at page 236 of the book for this reference ;; static parent

look at page 236 of the book for this reference ;; static ancestors

when a section of code allocate storage when the section is entered and deallocate it when the section is exited ;; block

blocks provide the origin of this phrase ;; block-structured language

based on the calling sequence of subprogams, not on their spatial relationship to each other ;; dynamic scoping

of a statement, is the collection of all variables that are visible in the statement ;; referencing environment

if a subprograms execution has begun but has not yet terminated ;; active

is a variable that is bound to a value only once ;; named constants