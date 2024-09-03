# Proofs 

Here is all of the proofs that are in the slides

## Chapter 1 

**Theorem**
The class of regular languages is closed under the union operation.
In other words, if A1 and A2 are regular languages, so is A1 ∪ A2.

**Proof Idea**
Construct M from M1 (that recognizes A1) and M2 (that recognizes A2).
Simulate both M1 and M2 simultaneously, and accept if either of the
simulations accept.

Remark: We can not “rewind the input tape” to try the simulation on M2

**Proof**
Let M1 recognize A1, where M1 = (Q1, Σ, δ1, q1, F1),
and M2 recognize A2, where M2 = (Q2, Σ, δ2, q2, F2).
Construct M to recognize A1 ∪ A2, where M = (Q, Σ, δ, q0, F ).
1. Q = {(r1, r2)|r1 ∈ Q1 and r2 ∈ Q2}.

This set is the Cartesian product of sets Q1 and Q2 and is written
Q1 × Q2.

2. Σ is the same as in M1 and M2.
3. δ((r1, r2), a) = (δ1(r1, a), δ2(r2, a)).
4. q0 = (q1, q2).
5. F = {(r1, r2)|r1 ∈ F1 or r2 ∈ F2}.

Remarks on the proof:
The last expression, F = {(r1, r2)|r1 ∈ F1 or r2 ∈ F2}, is the same as
F = (F1 × Q2) ∪ (Q1 × F2), which is not the same as F = F1 × F2
obviously.

F = F1 × F2 proves closure for intersection


![image](https://github.com/user-attachments/assets/7c027440-53ee-44bb-80ca-d0cb81b195e2)
