<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;"> Partial truth tables </h1>

<style>
  /* Add font-family to inherit from your main CSS */
  * {
    font-family: inherit;
  }

  h1 {
    text-align: center;
    font-size: 3rem;
    margin-bottom: 2rem; 
    margin-top: 3rem;
    font-family: inherit; /* Add this */
  }

  h2 {
    margin-top: 2.5rem;
    margin-bottom: 1rem;
    font-size: 2rem;
    font-family: inherit; /* Add this */
  }

  h3 {
    margin-top: 2rem;
    margin-bottom: 0.8rem;
    font-size: 1.5rem;
    font-family: inherit; /* Add this */
  }

  p {
    text-align: justify;
    margin-bottom: 1rem;
    line-height: 1.5;
    font-family: inherit; /* Add this */
  }

  ol {
    margin-left: 2rem;
    margin-bottom: 1.5rem;
    font-family: inherit; /* Add this */
  }

  ol li {
    margin-bottom: 0.5rem;
    font-family: inherit; /* Add this */
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

The idea of *partial truth tables* is that we don’t always need to list every possible input for a proposition in order to determine whether it is a tautology, contradiction, or something else. Instead, we can strategically test only the cases that matter. One common method is Reductio ad Absurdum ($raa$), in which we assume the opposite of what we want to prove and then show that this assumption leads to a contradiction.  

### 1. Example 1: Tautology

Consider the formula:  

$$ (a \land (a \rightarrow b)) \rightarrow b $$  

To test whether this is a tautology, we assume the formula is false. An implication $x \rightarrow y$ is false only when $x$ is true and $y$ is false.  

Firstly, we assume the implication is false:  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\land$</th>
      <th>$(a \rightarrow b)$</th>
      <th>$\rightarrow$</th>
      <th>$b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td></td>
      <td></td>
      <td></td>
      <td style="color:red;">0</td>
      <td></td>
    </tr>
  </tbody>
</table>

Second, since the implication is false, we can immediately set $b = \text{False}$. Moreover, the implication has two parts:

$$ (a \land (a \rightarrow b)) \quad \text{and} \quad b $$

By definition of implication, for the whole formula to be false the consequent $b$ must be false and the antecedent $(a \land (a \rightarrow b))$ must be true. Therefore, we place *True* under the Conjunction ($\land$) row.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\land$</th>
      <th>$(a \rightarrow b)$</th>
      <th>$\rightarrow$</th>
      <th>$b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td></td>
      <td style="color:green;">1</td>
      <td></td>
      <td style="color:red;">0</td>
      <td style="color:red;">0</td>
    </tr>
  </tbody>
</table>

Third, a conjunction is true only when both inputs are true. Thus, $a$ must be true and $(a \rightarrow b)$ must also be true. However, since we already assumed $b$ is false, the expression $(a \rightarrow b)$ becomes a contradiction.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\land$</th>
      <th>$(a \rightarrow b)$</th>
      <th>$\rightarrow$</th>
      <th>$b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="color:green;">1</td>
      <td style="color:red;">1</td>
      <td style="color:green;">1</td>
      <td style="color:red;">0</td>
      <td style="color:red;">0</td>
    </tr>
  </tbody>
</table>

Finally, as we can see, $(a \rightarrow b)$ would only be true when $b$ is true. Yet from the beginning we assumed $b$ is false. This creates a contradiction, so the statement cannot be false under any assignment of truth values. Therefore, the formula is always true, which means it is a tautology.  

### 2. Example 2: Contradiction  

To show a formula is a contradiction, we try to make the formula true by assigning truth values. If no assignment makes it true, it is a contradiction.  

Consider this formula:  

$$ a \land \neg a $$  

First, suppose $a = 1$. Then $\neg a = 0$.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\neg a$</th>
      <th>$a \land \neg a$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
    </tr>
  </tbody>
</table>

Second, suppose $a = 0$. Then $\neg a = 1$.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\neg a$</th>
      <th>$a \land \neg a$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
    </tr>
  </tbody>
</table>

Ultimately, in both cases, the output of $a \land \neg a$ is *False*. Therefore, the formula $a \land \neg a$ is never true and is a contradiction.  

### 3. Example 3: Equivalence  

To show two formulas are equivalent, we check whether they always have the same truth value under every possible assignment of inputs.  

Consider this equivalence:  

$$ a \rightarrow b \;\;\equiv\;\; \neg a \lor b $$  

Suppose $a = 1$ and $b = 1$.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$a \rightarrow b$</th>
      <th>$\neg a$</th>
      <th>$\neg a \lor b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
    </tr>
  </tbody>
</table>

Also, suppose $a = 1$ and $b = 0$.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$a \rightarrow b$</th>
      <th>$\neg a$</th>
      <th>$\neg a \lor b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
    </tr>
  </tbody>
</table>

Suppose $a = 0$ and $b = 1$.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$a \rightarrow b$</th>
      <th>$\neg a$</th>
      <th>$\neg a \lor b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
    </tr>
  </tbody>
</table>

Finally, suppose $a = 0$ and $b = 0$.  

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$a \rightarrow b$</th>
      <th>$\neg a$</th>
      <th>$\neg a \lor b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
    </tr>
  </tbody>
</table>

As a result, in every possible case, the columns for $a \rightarrow b$ and $\neg a \lor b$ match exactly. Therefore, the two formulas are logically equivalent.  

Full truth table:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th style="border: 2px solid red;">$a \rightarrow b$</th>
      <th style="border: 2px solid red;">$\neg a \lor b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green; border: 2px solid red;">1</td>
      <td style="text-align:center; color:green; border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red; border: 2px solid red;">0</td>
      <td style="text-align:center; color:red; border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green; border: 2px solid red;">1</td>
      <td style="text-align:center; color:green; border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green; border: 2px solid red;">1</td>
      <td style="text-align:center; color:green; border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

Note that to show that a formula is an entailment, we must present a complete truth table. We cannot just assume a few simple inputs, as is sometimes done with tautologies or contradictions.

### 4. Example 4: Validity

To check for validity using a partial truth table, we assume the conclusion is false and see if all premises can still be true. If it is impossible, the argument is valid.

Consider the argument:

1. $a \rightarrow b$  
2. $b \rightarrow c$  

We want to prove that $a \rightarrow c$.

First, assume the conclusion is false. To make $a \rightarrow c$ false, recall that a conditional statement $x \rightarrow y$ is false only when $x = 1$ and $y = 0$.  
Thus, we set:

$$
a = 1, \quad c = 0
$$

Next, we try to keep the premises true. For $a \rightarrow b$ to be true with $a = 1$, we must set:

$$
b = 1
$$

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$c$</th>
      <th>$a \rightarrow b$</th>
      <th>$b \rightarrow c$</th>
      <th>$a \rightarrow c$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:green;">1</td>
      <td style="text-align:center; color:red;">0</td>
      <td style="text-align:center; color:red;">0</td>
    </tr>
  </tbody>
</table>

1. $a \rightarrow b$ is *True*.  
2. $b \rightarrow c$ is *False*.  
3. $a \rightarrow c$ is *False* (as intended).  

Recall that for validity we require the premises $$a \rightarrow b \quad \text{and} \quad b \rightarrow c$$ to be *True*.  

However, when we force the conclusion to be false ($a=1, c=0$), one of the premises ($b \rightarrow c$) inevitably becomes false as well. Thus, it is impossible to make all the premises true while keeping the conclusion false. Therefore, the argument is valid.
