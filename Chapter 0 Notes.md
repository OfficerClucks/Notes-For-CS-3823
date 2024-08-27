# Chapter 0 Notes

A **set** is a collection of distinct elements.
 - Elements can be anything (numbers, symbols, strings, etc.).
 - Example: A = {7, 21, 57}

The **elements** of a set are also called **members** of the set;
- e.g., 7 ∈ {7, 21, 57}, 8 /∈ {7, 21, 57}

A ⊆ B: Denotes “A is a **subset** of B”

A ( B: Denotes “A is a **proper subset** of B”

The order and repetitions of the elements do *not* matter;
- e.g., {57, 7, 7, 7, 21} = {7, 21, 57}.

If we take the occurrences of members into account, we have a ***multiset***;
then {57, 7, 7, 7, 21} ≠ {7, 21, 57}.

Infinite sets: Sets with **infinite** elements;
- e.g., N = {1, 2, 3, . . .}, Z = {. . . , −2, −1, 0, 1, 2, . . .}

Empty set: ∅

## Operations on Sets
Union (∪): A ∪ B is the set of elements in either A or B (or both).

Intersection (∩): A ∩ B is the set of elements in both A and B.

Complement (A): A is the set of elements not in A.

Difference (\): A\B is the set of elements that belong to A but not B.

Difference (∆): A∆B is the set of elements that are either in set A or
in set B but not in both

### Formal Languages
In theoretical computer science, we use ***formal languages*** to describe sets of strings.

A formal language is defined over an alphabet.

Examples:
 - L = {0, 1} is the language containing only the strings "0" and "1".
 - L = {a, b, c}∗ is the language containing all possible strings formed from
the alphabet {a, b, c}.

Formal languages can have different properties, such as:

- **Regular languages**: Can be recognized by finite automata or regular
expressions.

- **Context-free languages**: Can be recognized by pushdown automata
or context-free grammars.

- **Decidable languages**: Have an algorithm that can determine
membership in the language.

- **Undecidable languages**: No algorithm can determine membership in
the language.

## Symbols and Notations
Mathematical symbols are used to represent operations, relations, and
variables.

Example notations:
- ∀: for all
- ∃: there exists
- ∃!: there exists a unique ...
- ⇒: implies
- ∈: is an element of

Logical operators are used to connect and manipulate statements.
Common logical operators:

- ¬: negation (not)
- ∧: conjunction (and)
- ∨: disjunction (or)
- ⇒: implication
- ⇔: equivalence


