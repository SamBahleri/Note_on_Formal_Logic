<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;"> Compound Statements </h1>

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

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; As we have learned in the Well-Formed Formula part, by using connectives such as $\neg$ , $\land$, $\lor$, $\rightarrow$, $\leftrightarrow$, we can create more complex combinations. Then, we can also calculate their truth values. For example:

### 1. Example 1

Let

$$(a \lor b) \land c$$

Where:  

− $a$: $2$ is prime  

− $b$: $2$ is even  

− $c$: $2$ is divisible by some even number  

Then, we want to check every possible truth value for $a$, $b$, and $c$ using a truth table.

First, we evaluate the $(a \lor b)$ expression:

Since $a$ is *True* and $b$ is also *True*, the output for $(a \lor b)$ is *True*, or $(a \lor b) = 1$.

Next, we check the value of $c$. Since it is true that $2$ is divisible by some even number, the value of $c$ is also *True*. Hence, $c = 1$.

Finally, by combining $(a \lor b)$ and $c$ with the conjunction operator ($\land$), we know that when both inputs are *True*, the output will also be *True*.

| $a$ | $b$ | $c$ | $(a \lor b)$ | $(a \lor b) \land c$ |
|---|---|---|-------|-------------|
| 1 | 1 | 1 |   1   |      1      |
| 1 | 1 | 0 |   1   |      0      |
| 1 | 0 | 1 |   1   |      1      |
| 1 | 0 | 0 |   1   |      0      |
| 0 | 1 | 1 |   1   |      1      |
| 0 | 1 | 0 |   1   |      0      |
| 0 | 0 | 1 |   0   |      0      |
| 0 | 0 | 0 |   0   |      0      |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Furthermore, because we already know that $2$ is prime, even, and divisible by some even number, the output is obviously *True* for the $(a \lor b) \land c$ combination. Moreover, since the expression is already known to be *True*, we do not need to consider the rest of the possible values in the truth table; in this case, we only take the first row.

### 2. Example 2

Let

$$ 
\begin{align*}
a &= \displaystyle\left[ x = 3, y = 5 \to 2^x \cdot 2^y = 2^5 \right]\\
b &= \left[p = 8, q = 6 \to \frac{2^p}{q^q} < \frac{2^p}{3^9}\right]\\
c &= \left[\left[3^{1/2}\right]^2 \cdot \left[2^{1/2}\right]^2 = 2^2+2 \right] 
\end{align*}$$

We ask for  

$$(a \to b) \land c$$

since

$$ a = 1, \quad b= 1, \quad c= 1$$

We conclude that

$$\boxed{((a \to b) \land c )= True}$$

### 3. Example 2

Let

$$
\begin{align*}
d &= \left[p=4 \;\to\; 2^p \cdot 2^5 = 2^9 \right] &
f &= \left[\frac{2^4 \cdot 3^6}{2^3 \cdot 3^2}\right]^3 = 2^3 \cdot 3^{12} \\[1mm]
e &= \left[p=3 \;\to\; (3\pi)^p = 27\pi^3 \right] &
g &= \left[\frac{1^{-1}}{5^{-6}} \right] = 5^6
\end{align*}
$$

We ask for  

$$
((d \leftrightarrow e) \lor f) \land g
$$

Since

$$
d = 1, \quad e = 1, \quad f = 1 , \quad g = 1
$$

Therefore

$$
\boxed{(((d \leftrightarrow e) \lor f) \land g )= True}
$$

### 4. Example 4

Let

$$
\begin{align*}
h &= \displaystyle\left[ x=2, \; y=5 \;\to\; \left[\frac{8 \cdot x^3 \cdot y^{-4}}{16 \cdot y^{-1/4}}\right]\right] 
      \;\to\; \neg \neg \left[\frac{4}{\sqrt[4]{5^{15}}}\right] \\[2mm]
i &= \displaystyle\left[\frac{2^5 \cdot 3^{-10}}{2^5 \cdot 3^{-4}}\right]^{1/2}
      \left[\frac{4^{1/4} \cdot 5^{1/2}} {4^{1/2} \cdot 5^{-1/2}}\right]^{1/2} \to \sqrt{\frac{5}{3^6 \cdot \sqrt{2}}}\\
j &= \displaystyle\left[p = 3, q = 3 \;\to\; \left[ 5 \sqrt{2^p} \cdot 3 \sqrt[q]{3} 
      \leftrightarrow 15 \cdot 2 \sqrt{2} \cdot \sqrt[3]{3} \right]\right]
\end{align*}
$$

We ask for

$$h \lor \neg \neg (i \land j)$$

Since

$$
h = 1, \quad i = 1, \quad f = 1 , \quad j = 1
$$

Hence

$$
\boxed{(h \lor \neg \neg (i \land j)) = True}
$$

### 5. Example 5

Let

$$ \begin{align*}
k &= \sqrt{2} + \sqrt{6} < \sqrt{15}\\
l &= \sqrt{8} + \sqrt{10} < \sqrt{40}\\
m &= \sqrt{5} + \sqrt{7} \ge \sqrt{26}\\
\end{align*}
$$

We ask for

$$(k \land l) \to m$$

since

$$
k = 1, \quad l = 1, \quad m = 0 ,
$$

Thus

$$
\boxed{(k \land l) \to m = False}
$$
