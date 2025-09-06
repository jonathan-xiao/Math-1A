## Open Sentences

An open sentence is not definitely true or false and has at least one free variable
 - Consider $x \leq 0$ as an open sentence

If an open statement $p$ regards the variable $x$, we write the open sentence as $p(x)$. We can also write $p(x_1, x_2, ..., x_n)$ for more variables. 

Open statements have scopes, which include the values that can be substituted for $x$. For examples, a scope could be the integers. 

When a value is inputted for $x$, like $p(3)$, then the open sentence becomes a statement. 

## Quantifiers

Quantifiers turn open sentences into statements. There are:

1. The Universal Quantifier ($\forall$)

   - $\forall x \in \mathbb{Z}, x \geq 0$
   - $\forall x \in A, p(x)$ is true only when every value in $A$ makes $p(x)$ true. Any counterexample in $A$ makes the statement false.

2. The Existential Quantifier ($\exists$)

   - $\exists x \in \mathbb{Z}, x \geq 0$
   - $\exists x \in A, p(x)$ is true if there is at least one $x \in A$ s.t. $p(x)$ is true. It is only false if every value of $x$ in $A$ makes $p(x)$ false.

Open sentences are statements only when every single variable in the sentence is quantified. 

 - $\forall x \in \mathbb{Z} \space \exists y \in \mathbb{Z}$ s.t. $x < y$ is a statement

These statements are read left to right and contain an open sentence in them, namely $x < y$ here.


## Set Theory

Every object in math is a set with the information needed to reason with the object. 

- A point on the 2-D plane could be $(x,y) = \\{\\{x\\}, \\{x,y\\}\\}$

It is assumed that the empty set exists, that is, a set with no elements inside. It is called $\emptyset$.

Sets are unordered, and they do not repeat identical elements. 

The natural numbers including 0 may be given as:

$0 = \emptyset$  
$1 = \\{\emptyset \\}$  
$2 = \\{\emptyset, \\{\emptyset \\} \\}$  

$n+1 = n \cup \\{n \\}$

Suppose that $A, B$ are sets. Then we can use set-builder notation to make a new set.

$$A \cap B = \\{x : x \in A \land x \in B \\}$$

This means $x$ s.t. $x$ is in $A$ and $x$ is in $B$.

We also have:

$$A \cup B = \\{x : x \in A \lor x \in B \\}$$

$$A \times B = \\{(x,y): x \in A \land y \in B\\}$$

The last is called the Cartesian Product, which is a set of all the ordered pairs where $x \in A$ and $y \in B$

We say $A$ is a subset of $B$ if every element in $A$ is also an element in $B$. Therefore: 

$$A \subseteq B \implies \forall x(x \in A \rightarrow x \in B)$$

Is true. 

## Relations

A relation on two sets $A,B$ is a subset of $A \times B$.

 - $R = \\{(n, \frac{1}{n}): n \in \mathbb{Z}, n \neq 0\\}$ is a relation on $\mathbb{Z} \times \mathbb{Q}$

If $R \subseteq A \times B$ then $(x,y) \in R$ means the same as $xRy$. 

## Functions

A function from $A$ to $B$ is a relation with two conditions.

1. $\forall a \in A$, $\exists b \in B$ s.t. $f(a) = b$.
2. "Well-defined": $\forall a \in A$ and $b,c \in B$, if $f(a)=b$ and $f(a)=c$ then $b=c$.

Function:

$f = \\{(x, x^2): x \in Z\\}$ for $\mathbb{Z}$ to $\mathbb{Z}$

Not a Function:

$R = \\{(n, \frac{1}{n}): n \in \mathbb{Z}, n \neq 0\\}$ is not a function on $\mathbb{Z} \times \mathbb{Q}$ because it lacks $n=0$ and $0 \in \mathbb{Z}$




















