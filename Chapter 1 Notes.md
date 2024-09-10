
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

---

NFAs:
- may have zero, one, or many arrows exiting from each state for each
alphabet symbol,

- may have zero, one, or many arrows exiting from each state with the
label λ

- NFA's Dont have to have all of the fail states like the DFA's do 

![image](https://github.com/user-attachments/assets/505efe88-bc59-41df-b474-a7888661131e)

A **nondeterministic finite automaton** is a 5-tuple (Q, Σ, δ, q0, F ), where
 - Q is a finite set of states,
- Σ is a finite alphabet,
- δ : Q × Σλ → P(Q) is the transition function,
- q0 ∈ Q is the start state, and
- F ⊆ Q is the set of accept states.
Note:
Σλ = Σ ∪ {λ}

P(Q) = powerset of Q

NFA's Work in this order:

- We reach a state with multiple ways to proceed.
⇒ the machine (automaton) splits into multiple copies of itself and
follows all the possibilities in parallel (each copy takes one of the
possible ways to proceed).

- We reach a state where no branch of the computation exiting from it
can compute the current symbol
⇒ the particular copy of the machine dies (along with the branch of
the computation associated with it.

- If any of the copies of the machine is in an accept state at the end of
the input, the NFA accepts the input string.
States with an λ symbol on an exiting arrow is encountered
⇒ splits into multiple copies.

Here is a tree showing the difference between dfa and nfa 

![image](https://github.com/user-attachments/assets/864187e1-870b-4d24-9a0a-d37a2b53f272)

Look to the slides for more examples but here are two that I found the most helpful.



![image](https://github.com/user-attachments/assets/fdf78b39-7072-4225-b414-51b1e24847f6)

![image](https://github.com/user-attachments/assets/31ec5a97-55ab-4096-9f92-1c6473743ac8)

---

When you are combining two or more NFA's  accepting states you remove the first NFA's accepting states and do a lambda transition to the starting state of the accepting state.

---

Definition

A **Generalized Nondeterministic Finite Automaton (GNFA)** is an NFA
wherein the transition arrows may have any regular expression as labels
(instead of only members of the alphabet or λ).

- The GNFA reads blocks of symbols from the input, not necessarily just
one symbol at a time (as in an ordinary NFA).

- The GNFA moves along a transition arrow connecting two states by
reading a block of symbols from the input; that string is a string that
corresponds to the regular expression on that arrow.

- A GNFA, being nondeterministic, may have several different ways to
process the same input string
