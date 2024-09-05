
# Chapter 1 Regular Languages

## Finite Automata 

Simplest computational model:
**Finite state machine** or **finite automaton**
- Good model for computers with extremely limited amount of memory
(e.g., automatic door).
- Markov chains are probabilistic counterparts of finite automata.

Finite Automaton Example (M1):

![image](https://github.com/user-attachments/assets/ff6c8063-e03e-43a1-b1e1-628739eb32db)

M1 recognizes strings that:
- have at least one 1,
- end in a 1,
- end in an even number of zeros, following the last 1 (i.e., there is at least one 1)

**Finite automaton**
A **finite automaton** is a 5-tuple (Q, Σ, δ, q0, F ), where:
- Q is a finite set called the **states**,
- Σ is a finite set called the (input) **alphabet**,
- δ : Q × Σ → Q is the **transition function** (it includes the rules for
moving),
- q0 ∈ Q is the **start state**, and
- F ⊆ Q is the **set of accept states** (final states).

A **Language** of machine M is the set of strings that M accepts.
- Notation: L(M) = A
  - We say that M recognizes A or that M accepts A

A language is called a **regular language** if some finite automaton
recognizes it.

### Regular Operations 

Let A and B be languages. We define the regular operations **union**,
**concatenation**, and **star** as follows:
- Union: A ∪ B = {x|x ∈ A or x ∈ B}.
- Concatenation: A ◦ B = {xy|x ∈ A and y ∈ B}.
- Star: A∗ = {x1x2 . . . xk |k ≥ 0 and each xi ∈ A}.

Remark: The empty string λ is always a member of A∗, no matter what A is.

A collection of objects is **closed** under some operation if applying that
operation to members of the collection returns an object still in the
collection.

The collection of regular languages is closed under all three of the
regular operations.

Example 6 (Closeness)

Let the alphabet Σ be the standard 26 letters {a, b, . . . , z}.

If A = {good, bad} and B = {boy, girl}, then

A ∪ B = {good, bad, boy, girl},

A ◦ B = {goodboy, goodgirl, badboy, badgirl}, 

A∗ = {λ, good, bad, goodgood, goodbad, badgood, badbad,
goodgoodgood, goodgoodbad, goodbadgood, goodbadbad, . . . }

NFAs:
- may have zero, one, or many arrows exiting from each state for each
alphabet symbol,

- may have zero, one, or many arrows exiting from each state with the
label λ

![image](https://github.com/user-attachments/assets/505efe88-bc59-41df-b474-a7888661131e)
