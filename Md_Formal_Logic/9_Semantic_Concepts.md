<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;"> Semantic concepts </h1>


<style>
  h1 {
    text-align: center;
    font-size: 3rem;
    margin-bottom: 2rem; 
    margin-top: 3rem;
  }

  h2 {
    margin-top: 2.5rem;
    margin-bottom: 1rem;
    font-size: 2rem;
  }

  h3 {
    margin-top: 2rem;
    margin-bottom: 0.8rem;
    font-size: 1.5rem;
  }

  p {
    text-align: justify;
    margin-bottom: 1rem;
    line-height: 1.5;
  }

  ol {
    margin-left: 2rem;
    margin-bottom: 1.5rem;
  }

  ol li {
    margin-bottom: 0.5rem;
  }

/* Flexible, centered, responsive table */
table {
  max-width: 700px;       /* cap width on large screens */
  width: 100%;            /* fill container on small screens */
  margin: 20px auto;      /* add 20px vertical space and center horizontally */
  border-collapse: collapse;
  table-layout: auto;
  font-size: 1.2rem;
}

/* Tables */
table {
  margin: 2rem auto;             /* center the table */
  border-collapse: collapse;
  width: auto;                   /* shrink to content instead of full width */
  text-align: center;
}

th, td {
  border: 1px solid #bcb7b7ff;
  padding: 0.6rem 1.2rem;
  text-align: center;
}

th {
  background-color: #d7d4d4ff;
  font-weight: bold;
}

/* Optional: center caption-like headings */
.table-title {
  text-align: center;
  font-weight: bold;
  margin-bottom: 1rem;
  font-size: 1.2rem;
}

</style>

</style>

In the previous chapter, we learned about symbols such as $p$, $q$, $\neg$, $\land$, $\lor$, $\to$, and $\leftrightarrow$, as well as the syntax rules that define well-formed formulas (wff), for example, $a \lor b$. In this chapter, we will explore semantics, which deals with the meaning and interpretation of these formulas.

### 1. Tautology

A formula is a tautology if it is always true, regardless of the truth values of its components. For example, $a \lor \neg a$ is a tautology; it remains true whether $a$ is *True* or *False*. Another example is $a \to a$, which is always *True* by the definition of implication. The symbol for tautology is usually denoted by $\top$. Hence, we can write tautologies such as:

$$
a \lor \neg a \quad (\top) \quad \text{and} \quad a \to a \quad (\top)
$$

Truth Tables:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\neg a$</th>
      <th>$a \lor \neg a$</th>
      <th style="border: 2px solid red;">$a \to a$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

### 2. Contradiction

A contradiction, frequently denoted by $\bot$, is a formula that is always *False*, no matter the truth values assigned. For example, $a \land \neg a$ is a contradiction because it can never be true. Another example is $(a \land \neg a) \lor (b \land \neg b)$, which is also always *False*.

Truth Table:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th>$\neg b$</th>
      <th>$a \land \neg a$</th>
      <th>$b \land \neg b$</th>
      <th style="border: 2px solid red;">$(a \land \neg a) \lor (b \land \neg b)$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
  </tbody>
</table>

### 3. Equivalence

In propositional logic, equivalence $(\equiv \text{ or } \leftrightarrow)$ between two well-formed formulas (wffs) means that they have the same truth value for all possible truth assignments to their propositions. If two formulas are logically equivalent, they will always evaluate to the same truth value, regardless of the truth values of the individual propositions.

For example, the formula $a \land b$ is equivalent to $\neg(\neg a \lor \neg b)$.

Truth Table:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th>$\neg b$</th>
      <th>$\neg a \lor \neg b$</th>
      <th style="border: 2px solid red;">$\neg(\neg a \lor \neg b)$</th>
      <th style="border: 2px solid red;">$a \land b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
  </tbody>
</table>

Common Forms of Logical Equivalence

1. Double Negation  
   $$\neg(\neg a) \equiv a$$

2. De Morgan’s Laws  
   $$\neg(a \land b) \equiv \neg a \lor \neg b$$  
   $$\neg(a \lor b) \equiv \neg a \land \neg b$$

3. Commutative Laws  
   $$a \land b \equiv b \land a$$  
   $$a \lor b \equiv b \lor a$$

4. Associative Laws  
   $$(a \land b) \land r \equiv a \land (b \land r)$$  
   $$(a \lor b) \lor r \equiv a \lor (b \lor r)$$

5. Distributive Laws  
   $$a \land (b \lor r) \equiv (a \land b) \lor (a \land r)$$  
   $$a \lor (b \land r) \equiv (a \lor b) \land (a \lor r)$$

6. Implication Equivalences  
   $$a \to b \equiv \neg a \lor b$$  
   $$\neg(a \to b) \equiv a \land \neg b$$

7. Biconditional (Equivalence)  
   $$a \leftrightarrow b \equiv (a \to b) \land (b \to a)$$  
   $$a \leftrightarrow b \equiv (a \land b) \lor (\neg a \land \neg b)$$

8. Contrapositive  
   $$a \to b \equiv \neg b \to \neg a$$

### 4. Contingency

A well-formed formula (wff) is called a contingency if it is *True* in some cases and *False* in others. In other words, it is neither a tautology nor a contradiction. For instance, $a \lor b$ is a contingency; it can be *True* or *False* depending on the values of $a$ and $b$.

Truth Table:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th style="border: 2px solid red;">$a \lor b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>

### 5. Satisfiability

Satisfiability refers to whether there exists *at least one* assignment of truth values to the variables in a formula that makes the formula *True*. A formula is satisfiable if it can be true for some assignment of its variables; otherwise, it is unsatisfiable. For example, the formula $a \land b$ is satisfiable because there is at least one assignment (when both $a$ and $b$ are *True*) that makes the formula true.

| $a$ | $b$ | $a \land b$ | $Satisfies?$ |
|-----|-----|-------------|--------------|
| 0   | 0   | 0           | $No$         |
| 0   | 1   | 0           | $No$         |
| 1   | 0   | 0           | $No$         |
| 1   | 1   | 1           | $Yes$        |

### 6. Validity

An argument is called *valid* if its conclusion necessarily follows from its premises, no matter whether the premises are true or false in the actual world. That is, in every case where the premises are true, the conclusion must also be true.  

For example, consider the statement:

$$
\neg a \to \neg b
$$  

Truth Table:  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th>$\neg b$</th>
      <th>$\neg a \to \neg b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr style="border: 2px solid red;">
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>  

In the last row, both $\neg a$ and $\neg b$ evaluate to *False*. Since the antecedent ($\neg a$) is *False*, the entire implication $\neg a \to \neg b$ evaluates to *True* according to the truth-table definition of implication. This truth arises because an implication with a *False* antecedent is always *True*, regardless of the consequent.

### 7. Soundness

An argument is sound if:
1. $\Gamma \vdash A$ (syntactic validity - provable)
2. $\Gamma \models A$ (semantic validity - tautological consequence)
3. All premises in $\Gamma$ are true

Soundness Theorem:

If $\Gamma \vdash A$, then $\Gamma \models A$

Equivalently:
1. If $\Gamma$ is satisfiable, then $\Gamma$ is consistent
2. Provability implies tautological consequence

Example

Given premises $\Gamma = \{a, b\}$ and conclusion $c$:

$$(a \land b) \to c$$

where:

− $a$: all birds have feathers  
− $b$: a robin is a bird  
− $c$: a robin has feathers  

Truth table:

| $a$ | $b$ | $c$ | $a \land b$ | $(a \land b) \to c$ |
|-----|-----|-----|-------------|----------------------|
| 1   | 1   | 1   | 1           | 1                   |
| 1   | 1   | 0   | 1           | 0                   |
| 1   | 0   | 1   | 0           | 1                   |
| 1   | 0   | 0   | 0           | 1                   |
| 0   | 1   | 1   | 0           | 1                   |
| 0   | 1   | 0   | 0           | 1                   |
| 0   | 0   | 1   | 0           | 1                   |
| 0   | 0   | 0   | 0           | 1                   |

In detail:
1. $\{a, b\} \vdash c$ (provable from premises)
2. $\{a, b\} \models c$ (tautological consequence)
3. $\varphi(a) = 1, \varphi(b) = 1, \varphi(c) = 1$ (all true in reality)
4. Therefore: the argument is sound

### 8. Entailment  

If validity refers to reasoning that is structurally correct but not necessarily factually accurate, and soundness refers to reasoning that is both valid and factually true, then *entailment* is a logical relationship where the truth of one statement necessarily guarantees the truth of another within a formal system. In other words, entailment shows that a conclusion must be true if the premises are true, based solely on the rules of logic.  

For example:  

$$ a \land b \models a $$  

This means that the statement $a \land b$ (both $a$ and $b$ are true) *entails* $a$ (that $a$ is true).  

Truth Table:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$a \land b$</th>
      <th>$a$</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border: 2px solid red;">
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>

Notice that in every case where $a \land b$ is true (the first row), the conclusion $a$ is also true. This illustrates the entailment: $a \land b$ logically entails $a$.

### 9. Completeness

Definition

A system is complete if

$$
\Gamma \models A \to \Gamma \vdash A
$$

Equivalently:

1. $\text{Cons}(\Gamma) \to \text{Sat}(\Gamma)$  
2. $\models \text{ then } \vdash$

Completeness Theorem

$$
\text{If } \Gamma \models A, \text{ then } \Gamma \vdash A
$$

Example

Let

$$
\Gamma = \{a \to b, \; a\}, \quad A = b
$$

Then

$$
\Gamma \models b
$$

By (MP):

$$
\frac{a \to b, \quad a}{b}
$$

Hence

$$
\Gamma \vdash b
$$
