# Sept 3: Statements and Truth Tables

## Statements

A mathematical statement is either true or false, meaning it has a truth value of either T or F
- 2 + 2 = 4 is true
- All primes are odd is false
- $x > 0$ is not a statement because it can be both depending on $x$

If $p$ is a statement, then $\lnot p$ is the negation
|$p$ |$\lnot$ $p$|
|---|:---:|
|T|F|
|F|T|

The negation must have the opposite truth value by the Law of the Excluded Middle.

If $p$ and $q$ are statements, then $p \land q$ is the conjunction

| $p$ | $q$ |$p$ $\land$ $q$|
|---|---|:---:|
|T|T|T                  |
|T|F|F|
|F|T|F|
|F|F|F|

If $p$ and $q$ are statements, then $p \lor q$ is the disjunction

| $p$ | $q$ | $p$ $\lor$ $q$ |
|---|---|:---:|
|T|T|T|
|T|F|T|
|F|T|T|
|F|F|F|

Note the inclusive use of OR. 

If $p$ and $q$ are statements, then $p \rightarrow q$ is the implication. If $p$ is true, then $q is true$. $p$ is called the anticedent, and $q$ the consequence.

| $p$ | $q$ | $p$ $\rightarrow$ $q$ |
|---|---|:---:|
|T|T|T|
|T|F|F|
|F|T|T|
|F|F|T|

Note the bottom columns are vacuously true. This means that something false implies anything, and we assume it true. "If pigs fly, I will give you 100 dollars" etc. 

For the statement $(p \rightarrow q) \land (q \rightarrow p)$, we have $p \leftrightarrow q$ which is "if and only if" (iff)

| $p$ | $q$ | $p$ $\leftrightarrow$ $q$ |
|---|---|:---:|
|T|T|T|
|T|F|F|
|F|T|F|
|F|F|T|

This is calso called the equivalence because it returns true only when $p$ and $q$ have the same truth value. 


## Sets

A set is a collection of objects
- For example, $\mathbb{Z} = \\{ ... , -1, 0, 1, 2, ...\\}$ is a set

If $A$ is a set and $a$ is an element, $a \in A$ means $a$ is an element of $A$ (or $a$ in $A$)


