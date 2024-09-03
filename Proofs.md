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
