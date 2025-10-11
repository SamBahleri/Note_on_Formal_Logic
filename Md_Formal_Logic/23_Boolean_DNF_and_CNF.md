<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem margin-bottom: 2rem;">Boolean, DNF, and CNF</h1>

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

.image-container {
text-align: center;
margin: 1.5rem 0;
width: 100%;
}

.responsive-image {
max-width: 100%;
height: auto;
width: 450px;
border-radius: 1px;
box-shadow: 0 2px 8px rgba(255, 255, 255, 1);
}

.image-caption {
font-style: italic;
font-size: 14px;
margin-top: 8px;
color: #666;
line-height: 1.4;
}

table {
max-width: 700px;
width: 100%;
margin: 20px auto;
border-collapse: collapse;
table-layout: auto;
font-size: 1.2rem;
}

table {
margin: 2rem auto;
border-collapse: collapse;
width: auto;
text-align: center;
background-color: #ffffffff
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

.table-title {
text-align: center;
font-weight: bold;
margin-bottom: 1rem;
font-size: 1.2rem;
}

/* Mobile Optimization */
@media (max-width: 768px) {
.image-container {
margin: 1rem 0;
padding: 0 0.5rem;
}

.responsive-image {
width: 100%;
max-width: 400px;
border-radius: 1px;
}

.image-caption {
font-size: 13px;
margin-top: 6px;
padding: 0 0.5rem;
}
}

/* Extra small mobile devices */
@media (max-width: 480px) {
.image-container {
margin: 0.8rem 0;
padding: 0 0.25rem;
}

.responsive-image {
max-width: 350px;
border-radius: 1px;
}

.image-caption {
font-size: 12px;
margin-top: 5px;
}
}

/* Large screens */
@media (min-width: 1200px) {
.responsive-image {
width: 500px;
}

.image-caption {
font-size: 15px;
}
}
</style>

## 1. Boolean

In short, the application of Boolean Algebra is essentially the same as Formal Logic. The main difference lies in the symbols used. For example, in Formal Logic, the symbol $\land$ is used for logical AND, whereas in Boolean Algebra we often use $\,\cdot\,$ (dot) for AND. Logical OR, represented by $\lor$ in Formal Logic, corresponds to $+$ in Boolean Algebra. Negation, $\neg x$ in Formal Logic, is written as $\bar{x}$ in Boolean Algebra.  Sometimes, you may also encounter the AND and OR symbols inside circles: $\oplus$ for XOR (exclusive OR) and $\odot$ or $\otimes$ for AND, depending on the text. These are just alternative notations and do not change the underlying logic.  

Furthermore, it is important to note that Boolean Algebra is not the same as conventional mathematics. Specifically, Boolean Algebra operates strictly on binary values ($1$ and $0$). General mathematics typically deals with a wider range of numbers, including integers, fractions, and complex numbers.  


| Property | Expression |
|----------|------------|
| Binary Operation $+$ | $1 + 0 = 1$ |
| Commutative Property of $+$ | $1 + 0 = 0 + 1$ |
| Associative Property of $+$ | $(1 + 0) + 1 = 1 + (0 + 1)$ |
| Binary Operation $\cdot$ | $1 \cdot 1 = 1$ |
| Commutative Property of $\cdot$ | $1 \cdot 0 = 0 \cdot 1$ |
| Associative Property of $\cdot$ | $(1 \cdot 0) \cdot 1 = 1 \cdot (0 \cdot 1)$ |
| Distributive Properties | $1 \cdot (0 + 1) = (1 \cdot 0) + (1 \cdot 1)$ |
| Special Combinations | $a = a \cdot (a + b)$ |
| Unary Operation $\bar{}$ (Negation) | $\bar{1} = 0, \bar{0} = 1$ |
| Identity with $+$ | $a + 0 = a$ |
| Annihilation with $\cdot$ | $a \cdot 0 = 0$ |
| Proof using Commutativity of $+$ | $a + b = b + a$ |
| Proof using Commutativity of $\cdot$ | $a \cdot b = b \cdot a$ |
| Identity Property of $+$ | $a + 0 = a$ |
| Zero for $+$ | $0 + a = a$ |
| Commutative Property for Zero | $0 + a = a + 0$ |
| Identity with $\cdot$ | $a \cdot 1 = a$ |
| Idempotent Law for $+$ | $a + a = a$ |
| Idempotent Law for $\cdot$ | $a \cdot a = a$ |
| Annihilation with $+$ | $a + 1 = 1$ |
| Annihilation with $\cdot$ | $a \cdot 0 = 0$ |
| Double Negation | $\overline{\overline{a}} = a$ |
| De Morgan's Law for $+$ | $\overline{a \cdot b} = \bar{a} + \bar{b}$ |
| De Morgan's Law for $\cdot$ | $\overline{a + b} = \bar{a} \cdot \bar{b}$ |

Let $k \geq 1$. A $k$-ary Boolean function $f$ takes as input $k$ True/False values and outputs a True/False value; namely, it is a mapping.

$$f : \{1, 0\}^k \rightarrow \{1, 0\}$$

Example:

$$f_{p_1 \cdot p_2}(x_1, x_2) = \begin{cases} 1 & \text{if } x_1 \text{ and } x_2 \text{ both equal } 1 \\ 0 & \text{otherwise} \end{cases}$$

Let $k \geq 1$ and let $A$ be a propositional formula that uses (at most) the variables $p_1, \ldots, p_k$. The $k$-ary Boolean function $f_A(x_1, x_2, \ldots, x_k)$ is defined by

$$f_A(x_1, \ldots, x_k) = \varphi(A), \text{ where } \varphi(p_i) = x_i \text{ for } i = 1, 2, \ldots, k$$

Construction:

$$f(x_1, x_2) = \begin{cases} 1 & \text{if } x_1 = 1 \text{ or } x_2 = 0 \\ 0 & \text{otherwise} \end{cases}$$

| $x_1$ | $x_2$ | $f(x_1, x_2)$ |
|-------|-------|---------------|
| $1$   | $1$   | $1$           |
| $1$   | $0$   | $1$           |
| $0$   | $1$   | $0$           |
| $0$   | $0$   | $1$           |

$$(p_1 \cdot p_2) + (p_1 \cdot \bar p_2) + (\bar p_1 \cdot \bar p_2)$$

### 1.2. General Construction

For $1 \leq i \leq 2^k$ and $1 \leq j \leq k$:

Form Disjunctions (Clauses):

$$\psi_i = \displaystyle\bigvee_{j=1}^k L_{i,j} := L_{i,1} + L_{i,2} + \cdots + L_{i,k}$$

Form Conjunctions (Clauses):

$$\Sigma_i = \displaystyle\bigwedge_{j=1}^k L_{i,j} := L_{i,1} \cdot L_{i,2} \cdot \cdots \cdot L_{i,k}$$

Example:

Let’s take two propositional variables:  
$$p_1, p_2$$

Possible truth assignments:

| $i$ | $p_1$ | $p_2$ |
|-----|:------:|:------:|
| 1 | 1 | 1 |
| 2 | 1 | 0 |
| 3 | 0 | 1 |
| 4 | 0 | 0 |

For each row $i$, we will form literals $L_{i,1}$ and $L_{i,2}$:
1. If $\varphi_i(p_j) = 1$, then $L_{i,j} = p_j$
2. If $\varphi_i(p_j) = 0$, then $L_{i,j} = \bar p_j$

Conjunction: 
$$
C_i = L_{i,1} \cdot L_{i,2}
$$

| $i$ | $(p_1, p_2)$ | $C_i$ |
|-----|:--------------:|:-------------|
| 1 | (1, 1) | $p_1 \cdot p_2$ |
| 2 | (1, 0) | $p_1 \cdot \bar p_2$ |
| 3 | (0, 1) | $\bar p_1 \cdot p_2$ |
| 4 | (0, 0) | $\bar p_1 \cdot \bar p_2$ |

Each $C_i$ corresponds to *one minterm*, True for exactly one assignment.

Disjunction:

$$
D_i = L_{i,1} + L_{i,2}
$$

| $i$ | $(p_1, p_2)$ | $D_i$ |
|-----|:--------------:|:-------------|
| 1 | (1, 1) | $p_1 + p_2$ |
| 2 | (1, 0) | $p_1 + \bar p_2$ |
| 3 | (0, 1) | $\bar p_1 + p_2$ |
| 4 | (0, 0) | $\bar p_1 + \bar p_2$ |

Each $D_i$ corresponds to *one maxterm*, False for exactly one assignment.

## 2. Disjunctive Normal Form (DNF)

The idea of DNF is that we can reduce all connectives in propositional logic (PL) to only $+ \ \text{(Disjucntion)}$, $.\ \text{(Conjunction)}$, and $\bar x \ \text{(negation)} $ in order to determine the truth value of a sentence. 

For example:

$$(s \cdot a) + (\bar m \cdot b) + (\bar h \cdot \bar l) + (r \cdot \bar i)$$

Moreover, for convenience we use $(\pm L)$ to indicate that $L$ is an atomic sentence which may or may not be prefaced with an occurrence of negation.
DNF example:

$$(\pm L_1 \cdot \dots \cdot \pm L_{i+1}) + (\pm L_j \cdot \dots \cdot \pm L_{k+1})$$

In detail:

Let $L$ be a sentence containing three atomic sentences $a, b, c$.

<table style="border-collapse: collapse;">
<thead>
<tr>
<th style="border: 1px solid black;">$a$</th>
<th style="border: 1px solid black;">$b$</th>
<th style="border: 1px solid black;">$c$</th>
<th style="border: 3px solid black;">$L$</th>
</tr>
</thead>
<tbody>
<tr style="border: 2px solid blue;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr style="border: 2px solid blue;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr style="border: 2px solid blue;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid blue;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">1</td>
</tr>
</tbody>
</table>

From the truth table, we observe that $L$ is true on lines $1, 3, 7, 8$. For each of these lines, we construct a conjunction that captures the exact truth value assignment on that line:

1. Line 1: $(a \cdot b \cdot c)$
2. Line 3: $(a \cdot \bar b \cdot c)$
3. Line 7: $(\bar a \cdot \bar b \cdot c)$
4. Line 8: $(\bar a \cdot \bar b \cdot \bar c)$

Therefore, a DNF representation logically equivalent to $L$ is:

$$(a \cdot b \cdot c) + (a \cdot \bar b \cdot c) + (\bar a \cdot \bar b \cdot c) + (\bar a \cdot \bar b \cdot \bar c)$$

This gives us a sentence in DNF which is true on exactly those lines where one of the disjuncts is true, namely, lines 1, 3, 7, and 8. Hence, the DNF sentence has exactly the same truth table as $L$. In other words, we have produced a sentence in DNF that is logically equivalent to $L$, which is precisely the goal of normalization.

### 2.1. General Construction

Let $L$ be a sentence containing atomic sentences $x_1, \dots, x_n$. We aim to construct a new sentence, $G$, that is *logically equivalent* to $L$ but written in DNF. Intuitively, $G$ will serve as a *truth-functional reconstruction* of $L$: it will reproduce the truth value of $L$ on every possible assignment of truth values to $x_1, \dots, x_n$. That is, for each possible line of the truth table for $L$, $G$ will be true if and only if $L$ is true on that line. Hence, $G$ acts as the DNF counterpart of $L$, the formula that expresses $L$'s truth behavior in canonical disjunctive form.

| Line | $x_1$ | $x_2$ | $\dots$ | $x_n$ | $L$ |
|:----:|:------:|:------:|:--------:|:------:|:----:|
| 1 | 1 | 1 | $\dots$ | 1 | $L_1$ |
| 2 | 1 | 1 | $\dots$ | 0 | $L_2$ |
| 3 | 1 | 0 | $\dots$ | 1 | $L_3$ |
| ⋮ | ⋮ | ⋮ | ⋮ | ⋮ | ⋮ |
| $2^n$ | 0 | 0 | $\dots$ | 0 | $L_{2^n}$ |

Case 1:

If $L$ is false on every line of its truth table, then $L$ is a contradiction. In that case, a contradiction of the form is in DNF and is logically equivalent to $L$.

Case 2:

If $L$ is true on at least one line of its truth table, we proceed as follows. For each line $i$ where $L = 1$, let $\psi_i$ be a conjunction of the form:

$$\psi_i = \displaystyle\bigwedge_{m=1}^{n} (\pm x_m)$$

where

$$
(\pm x_m) =
\begin{cases}
x_m, & \text{if } x_m = 1 \text{ on line } i, \\
\bar x_m, & \text{if } x_m = 0 \text{ on line } i.
\end{cases}
$$

That is, $x_m$ appears unnegated in $\psi_i$ if it is true on line $i$, and negated if it is false on line $i$. Thus, $\psi_i$ is true on, and only on, line $i$ of the truth table.

Now, let $i_1, i_2, \dots, i_j$ be the indices of all lines where $L = 1$. Then we define $G$ as the disjunction of all such $psi_i$:

$$G = \psi_{i_1} + \psi_{i_2} + \dots + \psi_{i_j} = \displaystyle\bigvee_{k=1}^{j} \left[ \bigwedge_{m=1}^{n} (\pm x_m) \right]$$

Since $G$ is a disjunction of conjunctions of literals, $G$ is in DNF. By construction, $L$ and $G$ are true on exactly the same lines of the truth table, and therefore

$$L \equiv G$$

Example:

Let $S$ contain three atomic sentences $x_1, x_2, x_3$.

<table style="border-collapse: collapse;">
<thead>
<tr>
<th style="border: 1px solid black;">$x_1$</th>
<th style="border: 1px solid black;">$x_2$</th>
<th style="border: 1px solid black;">$x_3$</th>
<th style="border: 3px solid black;">$S$</th>
</tr>
</thead>
<tbody>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">1</td>
</tr>
</tbody>
</table>

$S = 1$ on lines 1, 3, 7, and 8.

1. For line 1:$f_1 = (x_1 \cdot x_2 \cdot x_3)$
2. For line 3:$f_3 = (x_1 \cdot \bar x_2 \cdot x_3)$
3. For line 7:$f_7 = (\bar x_1 \cdot \bar x_2 \cdot x_3)$
4. For line 8:$f_8 = (\bar x_1 \cdot \bar x_2 \cdot \bar x_3)$

Form the disjunction:
$$B = f_1 + f_3 + f_7 + f_8$$

Hence,

$$\big[(x_1 \cdot x_2 \cdot x_3) + (x_1 \cdot \bar x_2 \cdot x_3) + (\bar x_1 \cdot \bar x_2 \cdot x_3) + (\bar x_1 \cdot \bar x_2 \cdot \bar x_3)\big]$$

We conclude that,
$$S \equiv B$$

## 3. Conjunctive Normal Form (CNF)

Shortly, the formal definition of CNF is also analogous to the definition of DNF.

For example:

$$(s + a) \cdot (\bar m + b) \cdot (\bar h + \bar l) \cdot (r + \bar i)$$

and

$$(\pm T_1 + \dots + \pm P_m) \cdot (\pm T_i + \dots + \pm T_k)$$

In detail:

Consider a sentence $T$ with atomic sentences $p, q, r$.

<table style="border-collapse: collapse;">
<thead>
<tr>
<th style="border: 1px solid black;">$p$</th>
<th style="border: 1px solid black;">$q$</th>
<th style="border: 1px solid black;">$r$</th>
<th style="border: 3px solid black;">$B$</th>
</tr>
</thead>
<tbody>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">1</td>
</tr>
</tbody>
</table>

The truth table shows $T$ is false on lines $2, 4, 6$. We build a clause for each false row by taking the disjunction of literals that would make that row true:

1. Line 2: $(\bar p + \bar q + r)$
2. Line 4: $(\bar p + q + r)$
3. Line 6: $(p + \bar q + r)$

A CNF formula logically equivalent to $T$:

$$(\bar p + \bar q + r) \cdot (\bar p + q + r) \cdot (p + \bar q + r)$$

Each clause eliminates exactly one false row. The conjunction ensures all three clauses hold simultaneously, making the formula false precisely where $M$ is false and true elsewhere.

### 3.1. General Construction

Given sentence $L$ with atomic sentences $y_1, \dots, y_n$, we construct an equivalent sentence $H$ in CNF. The strategy: identify where $L$ fails and build clauses that fail at exactly those points.

| Line | $y_1$ | $y_2$ | $\dots$ | $y_n$ | $L$ |
|:----:|:------:|:------:|:--------:|:------:|:----:|
| 1 | 1 | 1 | $\dots$ | 1 | $L_1$ |
| 2 | 1 | 1 | $\dots$ | 0 | $L_2$ |
| 3 | 1 | 0 | $\dots$ | 1 | $L_3$ |
| ⋮ | ⋮ | ⋮ | ⋮ | ⋮ | ⋮ |
| $2^n$ | 0 | 0 | $\dots$ | 0 | $L_{2^n}$ |

Case 1:

When $L$ is true everywhere, it is a tautology. Any tautological formula in CNF serves as an equivalent, such as $(p + \bar{p})$ or any logically equivalent tautology.

Case 2:

When $L$ is false on some lines, for each line $j$ where $L = 0$, construct clause $\phi_j$:

$$\phi_j = \displaystyle\bigvee_{t=1}^{n} (\pm y_t)$$

where

$$
(\pm y_t) =
\begin{cases}
\bar y_t, & \text{if } y_t = 1 \text{ on line } j, \\
y_t, & \text{if } y_t = 0 \text{ on line } j.
\end{cases}
$$

Each literal is the opposite of its truth value on line $j$, making $\phi_j$ false only on line $j$.

Let $j_1, j_2, \dots, j_s$ index all lines where $L = 0$. Define:

$$H = \phi_{j_1} \cdot \phi_{j_2} \cdot \dots \cdot \phi_{j_s} = \displaystyle\bigwedge_{w=1}^{s} \left[ \bigvee_{t=1}^{n} (\pm y_t) \right]$$

$H$ is in CNF. Since $H$ is false exactly where $L$ is false:

$$L \equiv H$$

Example:

Let $R$ have atomic sentences $y_1, y_2, y_3$.

<table style="border-collapse: collapse;">
<thead>
<tr>
<th style="border: 1px solid black;">$y_1$</th>
<th style="border: 1px solid black;">$y_2$</th>
<th style="border: 1px solid black;">$y_3$</th>
<th style="border: 3px solid black;">$R$</th>
</tr>
</thead>
<tbody>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">1</td>
</tr>
<tr style="border: 2px solid red;">
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 3px solid black;">0</td>
</tr>
<tr>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 3px solid black;">1</td>
</tr>
</tbody>
</table>

$R = 0$ on lines 2, 5, and 7.

1. For line 2: $g_2 = (\bar y_1 + \bar y_2 + y_3)$
2. For line 5: $g_5 = (y_1 + \bar y_2 + \bar y_3)$
3. For line 7: $g_7 = (y_1 + y_2 + \bar y_3)$

Form the conjunction:
$$C = g_2 \cdot g_5 \cdot g_7$$

Hence,

$$\big[(\bar y_1 + \bar y_2 + y_3) \cdot (y_1 + \bar y_2 + \bar y_3) \cdot (y_1 + y_2 + \bar y_3)\big]$$

We conclude that,
$$R \equiv C$$

Example 1:

Let

$$I = a \to \bar b$$

First, we rewrite using the definition of implication:

$$I = (a \to \bar b \equiv \bar a + \bar b)$$

Truth Table

<table style="border-collapse: collapse; text-align: center;">
<thead>
<tr>

<th style="border: 1px solid black;">$a$</th>
<th style="border: 1px solid black;">$b$</th>
<th style="border: 1px solid black;">$\bar a$</th>
<th style="border: 1px solid black;">$\bar b$</th>
<th style="border: 2px solid black;">$I$</th>
</tr>
</thead>
<tbody>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 2px solid red;">0</td>
<td style="border: 2px solid red;">0</td>
<td style="border: 2px solid black;">0</td>
</tr>
<tr>
<td style="border: 2px solid blue;">1</td>
<td style="border: 2px solid blue;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 2px solid black;">1</td>
</tr>
<tr>
<td style="border: 2px solid blue;">0</td>
<td style="border: 2px solid blue;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 2px solid black;">1</td>
</tr>
<tr>
<td style="border: 2px solid blue;">0</td>
<td style="border: 2px solid blue;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 2px solid black;">1</td>
</tr>
</tbody>
</table>

Hence,

1. DNF Construction:

    1. Line 2: $(a \cdot \bar b)$
    2. Line 3: $(\bar a \cdot b)$
    3. Line 4: $(\bar a \cdot \bar b)$

    Therefore,

    $$I= (a \cdot \bar b) + (\bar a \cdot b) + (\bar a \cdot \bar b)$$

2. CNF Construction:

    1. Line 1: $(\bar a + \bar b)$  

    Thus,  

    $$I= (\bar a + \bar b)$$

3. Both forms are logically equivalent:

    $$I \equiv \bar a + \bar b$$

Example 2:

Let

$$X = \neg(p \equiv q)$$

First, we rewrite using the definition of biconditional:

$$p \leftrightarrow q \equiv (p \cdot q) + (\bar{p} \cdot \bar{q})$$

Then, applying negation:

$$
\neg(p \leftrightarrow q) \equiv \neg[(p \cdot q) + (\bar{p} \cdot \bar{q})]
$$  

Using De Morgan’s law:

$$
X = (\bar{p} + \bar{q}) \cdot (p + q)
$$  

Truth Table

<table style="border-collapse: collapse; text-align: center;">
<thead>
<tr>
<th style="border: 1px solid black;">$p$</th>
<th style="border: 1px solid black;">$q$</th>
<th style="border: 1px solid black;">$\bar p$</th>
<th style="border: 1px solid black;">$\bar q$</th>
<th style="border: 1px solid black;">$p \equiv q$</th>
<th style="border: 2px solid black;">$X$</th>
</tr>
</thead>
<tbody>
<tr>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 2px solid red;">0</td>
<td style="border: 2px solid red;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 2px solid black;">0</td>
</tr>
<tr>
<td style="border: 2px solid blue;">1</td>
<td style="border: 2px solid blue;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 2px solid black; ">1</td>
</tr>
<tr>
<td style="border: 2px solid blue;">0</td>
<td style="border: 2px solid blue;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 1px solid black;">0</td>
<td style="border: 2px solid black; ">1</td>
</tr>
<tr>
<td style="border: 2px solid red;">0</td>
<td style="border: 2px solid red;">0</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 1px solid black;">1</td>
<td style="border: 2px solid black;">0</td>
</tr>
</tbody>
</table>

1. DNF Construction

    $X = 1$ on lines 2 and 3.

    1. Line 2: $(p \cdot \bar{q})$
    2. Line 3: $(\bar{p} \cdot q)$

    Therefore,  

    $$
    X = (p \cdot \bar{q}) + (\bar{p} \cdot q)
    $$  

2. CNF Construction

    $X = 0$ on lines 1 and 4.

    1. Line 1: $(\bar{p} + \bar{q})$
    2. Line 4: $(p + q)$

    Thus,

    $$
    X = (\bar{p} + \bar{q}) \cdot (p + q)
    $$  

3. Both forms are logically equivalent

    $$
    X \equiv (p \cdot \bar{q}) + (\bar{p} \cdot q) \equiv (\bar{p} + \bar{q}) \cdot (p + q)
    $$
