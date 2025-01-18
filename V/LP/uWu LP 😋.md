# Compiler Design To-Do List

This document outlines a to-do list for key compiler design topics, broken down into individual subtopics for better organization.

## 1. Phases of Compiler with Example

-   [ ] Understand the lexical analysis phase (scanning) with examples.
-   [ ] Understand the syntax analysis phase (parsing) with examples.
-   [ ] Understand the semantic analysis phase with examples.
-   [ ] Understand the intermediate code generation phase with examples.
-   [ ] Understand the code optimization phase with examples.
-   [ ] Understand the code generation phase with examples.
-   [ ] Trace the compilation of a simple program through all phases.

## 2. Finite Automata Problems

-   [ ] Design DFAs for given regular expressions.
-   [ ] Design NFAs for given regular expressions.
-   [ ] Convert NFAs to DFAs (Subset Construction).
-   [ ] Minimize DFAs (Table-Filling Algorithm).
-   [ ] Solve problems involving regular languages and finite automata.

## 3. Ambiguous Grammar and Elimination of Ambiguity (Left Recursion & Left Factoring)

-   [ ] Identify ambiguous grammars.
-   [ ] Understand the problems caused by ambiguity.
-   [ ] Eliminate left recursion (direct and indirect).
-   [ ] Perform left factoring.
-   [ ] Practice converting ambiguous grammars to unambiguous ones.

## 4. Parsing Techniques (Shift-Reduce Parsing, SLR parsing, CLR Parsing, LALR Parsing)

-   [ ] Understand the concept of shift-reduce parsing.
-   [ ] Construct parse trees using shift-reduce parsing.
-   [ ] Understand SLR parsing and construct SLR parsing tables.
-   [ ] Understand CLR parsing and construct CLR parsing tables.
-   [ ] Understand LALR parsing and construct LALR parsing tables.
-   [ ] Compare and contrast SLR, CLR, and LALR parsing.
-   [ ] Solve parsing problems using different techniques.

## 5. Attribute Grammar (L-attributed Definition, S-attributed Definition)

-   [ ] Understand the concept of attribute grammars.
-   [ ] Define S-attributed grammars and their evaluation.
-   [ ] Define L-attributed grammars and their evaluation.
-   [ ] Develop attribute grammars for simple language constructs.
-   [ ] Differentiate between synthesized and inherited attributes.

## 6. Bottom-up Evaluation of Attribute Grammar

-   [ ] Understand the bottom-up evaluation process for S-attributed grammars.
-   [ ] Implement a bottom-up evaluator for a simple grammar.
-   [ ] Understand the use of parse stacks in bottom-up evaluation.

## 7. Intermediate Codes (Syntax Tree, Three Address Codes, Triples, Indirect Triples, Quadruples)

-   [ ] Construct syntax trees for given code snippets.
-   [ ] Generate three-address code from syntax trees.
-   [ ] Represent intermediate code using triples.
-   [ ] Represent intermediate code using indirect triples.
-   [ ] Represent intermediate code using quadruples.
-   [ ] Convert between different intermediate code representations.

## 8. Symbol Table Implementation

-   [ ] Understand the purpose of a symbol table.
-   [ ] Implement a symbol table using various data structures (e.g., hash tables, linked lists, trees).
-   [ ] Understand the scope management in symbol tables.
-   [ ] Implement scope handling in a symbol table.

## 9. Code Optimization Techniques

-   [ ] Understand common code optimization techniques:
    -   [ ] Constant folding and propagation.
    -   [ ] Common subexpression elimination.
    -   [ ] Dead code elimination.
    -   [ ] Loop optimization (code motion, strength reduction, loop unrolling).
    -   [ ] Inline expansion.
-   [ ] Apply optimization techniques to given code examples.

## 10. Code Generation Algorithm

-   [ ] Understand the basic principles of code generation.
-   [ ] Develop a simple code generation algorithm for a target machine (e.g., assembly language).
-   [ ] Handle different data types and control flow structures in code generation.
-   [ ] Understand register allocation strategies.

This comprehensive to-do list should provide a structured approach to learning compiler design. Remember to revisit and review these topics regularly.


# Code Generation Algorithm
is the process of converting intermediate representation of the source code into target machine code.
Its primary goal is to produce efficient and correct machine code that adheres to the rules of target architecture.

1. Input to Code Generation
	1. The input to the code generator is the intermediate representation, which is the form of a graph like structure like a syntax tree or a DAG, the target code must execute the computation detailed in it
2. Target Code Requirements
	1. 