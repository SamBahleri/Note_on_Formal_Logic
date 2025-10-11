# Semantic Concepts for FOL

### 1. Validity

$$\text{A formula is valid if it's true in every interpretation}$$

Example: $$\forall x \in \{1,2,3\} \, (P(x) \rightarrow P(x))$$

This is valid because *if 1 has property $P$, then 1 has property $P$* is always true, regardless of what $P$ represents.

### 2. Satisfiability

$$\text{A formula is satisfiable if there exists at least one interpretation that makes it true}$$

Example: $$\exists x \in \{1,2,3\} \, (x > 1 \wedge x < 3)$$

This is satisfiable because we can choose $x = 2$, making *2 > 1 and 2 < 3* true.

### 3. Contradiction

$$\text{A formula is unsatisfiable if no interpretation can make it true}$$

Example: $$\exists x \in \{1,2,3\} \, (x > 3 \wedge x < 1)$$

This is unsatisfiable because no number in our domain can be both greater than 3 and less than 1.

### 4. Entailment

$$\Gamma \models \phi \text{ if } \phi \text{ is true whenever all formulas in } \Gamma \text{ are true}$$

Example: $$\{\forall x \in \{1,2,3\} \, (x < 3), 2 \in \{1,2,3\}\} \models (2 < 3)$$

The premises *all numbers in our set are less than 3* and *2 is in our set* entail *2 is less than 3*.

### 5. Non-Entailment

$$\Gamma \not\models \phi \text{ if there exists an interpretation where } \Gamma \text{ is true but } \phi \text{ is false}$$

Example: $$\{\exists x \in \{1,2,3\} \, (x > 1)\} \not\models \forall x \in \{1,2,3\} \, (x > 1)$$

*Some number is greater than 1* doesn't entail *all numbers are greater than 1* because 1 itself isn't greater than 1.

### 6. Joint Satisfiability

$$\text{Formulas are jointly satisfiable if some interpretation makes them all true simultaneously}$$

Example: $$\{P(1), \neg P(2), \exists x \, P(x)\} \text{ where domain } = \{1,2\}$$

We can make P true for 1, false for 2, and *something has property $P$* true, all consistent.

### 7. Logical Equivalence

$$\phi \equiv \psi \text{ if } \phi \text{ and } \psi \text{ have the same truth value in every interpretation}$$

Example: $$\forall x \in \{1,2,3\} \, \neg(x > 2) \equiv \forall x \in \{1,2,3\} \, (x \leq 2)$$

*No number is greater than 2* is equivalent to *every number is less than or equal to 2*.

### 8. Contingency

$$\text{A formula is contingent if it's true in some interpretations and false in others}$$

Example: $$\exists x \in \{1,2,3\} \, (x = 2)$$

This is contingent, true when our domain includes 2, false if we change the domain to $\{4,5,6\}$.

### 9. Expressibility

$$\text{A property is expressible if there exists a formula that captures exactly that property}$$

Example: $$\text{Even}(x) := (x = 2) \vee (x = 4) \text{ over domain } \{1,2,3,4\}$$

The property *being even* is expressible because we can write a formula true exactly for even numbers.

### 10.  Definability

$$\text{A relation is definable if it can be expressed using existing predicates and logical operators}$$

Example: $$\text{Between}(x,y,z) := (x < y < z) \vee (z < y < x) \text{ over } \{1,2,3,4,5\}$$

Using the less-than relation, we can define *$y$ is between $x$ and $z$* without introducing new predicates.

### 11. Implicit Definability 

$$\text{A relation is uniquely determined by certain conditions without explicit construction}$$

Example: $$\forall x,y \, (\text{Succ}(x,y) \leftrightarrow (x < y \wedge \neg\exists z \, (x < z < y)))$$

The successor relation in $\{1,2,3\}$ is implicitly defined as the unique immediate-next relation.

### 12. Finite Expressibility

$$\text{Properties expressible only over finite domains of specific size}$$

Example: $$\exists x \exists y \exists z \, (x \neq y \neq z \wedge \forall w \, (w = x \vee w = y \vee w = z))$$

*Having exactly 3 elements* can be expressed for domain $\{1,2,3\}$ but doesn't work for arbitrary domains.

### 13. Cardinality Constraints

$$\text{Expressing numerical constraints on elements satisfying properties}$$

Example: $$\exists x \exists y \, (x \neq y \wedge \text{Prime}(x) \wedge \text{Prime}(y)) \text{ over } \{2,3,4,5,6\}$$

This expresses *at least two distinct elements are prime* using existential quantification with inequality.