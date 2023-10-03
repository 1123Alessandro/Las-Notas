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