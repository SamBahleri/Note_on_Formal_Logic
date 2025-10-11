# Truth Table

As discussed in the section on symbolization, the purpose of using symbolic logic is to express the truth of a statement in a formal way. Then, by using these symbols, we can avoid the ambiguity of natural language. Moreover, the first thing to know is that every proposition, whether simple or compound, only represents either *true* or *false*.

$$
p = \begin{cases}
\text{1} \\
\text{0}
\end{cases}
$$

$$
q = \begin{cases}
\text{1} \\
\text{0}
\end{cases}
$$

Furthermore, if we combine these symbols with connectives, the output is also either true or false. In this case, truth tables are very useful for representing the possible values of a proposition.

### 1. Truth Table for Disjunction 

|  $p$  |  $q$  | $p \lor q $|
|:--:|:--:|:-----:|
|  1  |  1  |   1   |
|  1  |  0  |   1   |
|  0  |  1  |   1   |
|  0  |  0  |   0   |

<div align="center" style="margin-bottom: 20px;">
  <em>Disjunction is false only when both propositions are false</em>
</div>

### 2. Truth Table for Conjunction 

|  $x$| $y$  | $x \land y$ |
|---|---|:-----:|
| 1 | 1 |   1   |
| 1 | 0 |   0   |
| 0 | 1 |   0   |
| 0 | 0 |   0   |

<div align="center" style="margin-bottom: 20px;">
  <em>Conjunction is true only when both propositions are true.</em>
</div>

### 3. Truth Table for Implication 

| $r$ | $w$| $r \rightarrow w$ |
|---|---|:-----:|
| 1 | 1 |   1   |
| 1 | 0 |   0   |
| 0 | 1 |   1   |
| 0 | 0 |   1   |

<div align="center" style="margin-bottom: 20px;">
  <em>Implication is false only when the premise is true but the conclusion is false.</em>
</div>

### 4. Truth Table for Negation 

| $p$ | $ \neg p$ |
|---|:--:|
| 1 | 0  |
| 0 | 1  |

<div align="center" style="margin-bottom: 20px;">
  <em>The function of negation is to negate each proposition.</em>
</div>

### 5. Truth Table for Biconditional

| $p$ | $q$ | $p \leftrightarrow d$ |
|---|---|:-----:|
| 1 | 1 |   1   |
| 1 | 0 |   0   |
| 0 | 1 |   0   |
| 0 | 0 |   1   |

<div align="center" style="margin-bottom: 20px;">
  <em>Biconditional is true when both propositions have the same truth value.</em>
</div>

### 6. Truth Table for NAND

| $p$ | $q$ | $p \uparrow q$ |
|---|---|:-----:|
| 1 | 1 |   0   |
| 1 | 0 |   1   |
| 0 | 1 |   1   |
| 0 | 0 |   1   |

<div align="center" style="margin-bottom: 20px;">
  <em>NAND (Not AND) is false only when both $p$ and $q$ are true.</em>
</div>

### 7. Truth Table for NOR

| $p$ | $q$ | $p \downarrow q$ |
|---|---|:-----:|
| 1 | 1 |   0   |
| 1 | 0 |   0   |
| 0 | 1 |   0   |
| 0 | 0 |   1   |

<div align="center" style="margin-bottom: 20px;">
  <em>NOR (Not OR) is true only when both $p$ and $q$ are false.</em>
</div>

Recall that earlier, we saw statements in symbolic logic, such as $p \lor q $, $x \land y$, $ \neg p$, $r \rightarrow w$ and $p \leftrightarrow d$. Using the truth table, we can evaluate each of these statements.

Example 1:

$$p \lor q$$

Where:

− $ \text{p: 1+1 = 2, and this statement is true (1)}$

− $ \text{q: 3-2=1, and this statement is also true (1)}$

| $p$ | $q$ | $p \lor q$  |
|:--:|:--:|:----:|
| 1 | 1  |  1   |

Result: True $(1)$

Example 2:

$$x \land y$$

Where:

− $ \text{x : 1 < 2, and this statement is true (1)}$

− $ \text{y: 3 > 2, and this statement is also true (1)}$

| $x$ | $y$ | $x \land y$ |
|---|---|:-----:|
| 1 | 1 |   1   |

Result: True $(1)$

Example 3:

$$r \rightarrow w$$

Where:

− $ \text{r: It is raining, and this statement is true (1) }$

− $ \text{w: It is wet, and this statement is false (0)}$

| $r$ | $w$ |$r \rightarrow w$|
|---|---|:-----:|
| 1 | 0 |   0   |

Result: False (0)

Another important point to understand is that if we have a number of propositions and want to determine the truth value of each one, every proposition has two possible truth values: true $(1)$ or false $(0)$. Therefore, the total number of possible combinations of truth values for all the propositions is given by $2^n$, where $n$ is the number of propositions.
For example:

Possible Combinations for 2 Propositions ($2^2 = 4$)

<table>
  <thead>
    <tr>
      <th>$p$</th>
      <th>$q$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>

Possible Combinations for 3 Propositions ($2^3 = 8$)

<table>
  <thead>
    <tr>
      <th>$p$</th>
      <th>$q$</th>
      <th>$r$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
