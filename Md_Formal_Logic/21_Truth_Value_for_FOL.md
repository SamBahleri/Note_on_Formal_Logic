<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;">Truth Value for FOL</h1>
<!-- Remove the h1 rule from the <style> block -->

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
  
</style>

In propositional logic (PL), every atomic sentence is directly assigned a truth value (true or false). On the other hand, in first-order logic (FOL), the truth value of a predicate is determined relative to an interpretation and a variable assignment.

For example:

Let domain $D = \{1,2,3\}$, for $E(x)$ = "$x$ is even".

Hence:

− $E(1) =$ False

− $E(2) =$ True

− $E(3) =$ False

### 1. Example 1

Let the domain:
$$D = \{\langle x,y \rangle \in \mathbb{N}^2\}$$

Evaluate:
$$\forall x,y  \in D \;(x \cdot y > x + y)$$

However, by antisymmetric schema,  we can find a counterexample:

$$
\exists x \exists y \;\big((\langle x, y \rangle \in \mathbb{N}^2) \;\land\; x = y \;\land\; x = 2 \;\land\; y = 2 \;\land\; (x \cdot y = x + y) \;\land\; \neg(x \cdot y > x + y)\big)
$$

Therefore:
$$\boxed{\neg \forall x,y \in D \;(x \cdot y > x + y)}$$

Note that other counterexamples include $\langle 1,1 \rangle$, $\langle 1,2 \rangle$, $\langle 2,1 \rangle$, and $\langle 1,n \rangle$ for any $n \in \mathbb{N}$.

### 2. Example 2

Let the domain:
$$D = \mathbb{Z}$$

Evaluate:

$$\forall x \forall y \forall z \;(x, y, z \in \mathbb{Z} \to ((x + y = z) \to z > 0))$$

However, we can find a counterexample:

$$\exists x \exists y \exists z \;(x, y, z \in \mathbb{Z} \;\land\; x = -1 \;\land\; y = -2 \;\land\; z = -3 \;\land\; (x + y = z) \;\land\; \neg(z > 0))$$

Since $-3 \not> 0$, we have shown that there exist integers where the sum equals $z$ but $z$ is not positive.

Consequently:

$$\boxed{\neg \forall x \forall y \forall z \;((x + y = z) \to z > 0)}$$

### 3. Example 3

Let the domain:

$$
D = \displaystyle\left\{ x \in \mathbb{Z} \;\middle|\; \frac{3x}{2} + 1 + \frac{4x}{3} = -\frac{31}{8} + \frac{2x}{3} \right\}.
$$

Evaluate:

$$
\exists x \,(x \in D).
$$

Since $-\tfrac{9}{4} \notin \mathbb{Z}$,

Thus:

$$
\boxed{D = \varnothing}
$$

And the statement is false, because the domain is empty.

### 4. Example 4

Let the domain:
$$D = \{\langle x,y \rangle \in \mathbb{R}^2 \mid x + 2y = 16\} $$

Evaluate:

$$ \forall  x, y \in D \, ((x \in \mathbb{R} \land y \in \mathbb{Z}) \to x > y) $$

Since we can find a counterexample:

$$\exists x \exists y \;(x \in \mathbb{R} \;\land\; y \in \mathbb{Z} \;\land\; x = 0 \;\land\; y = 8 \;\land\; (x + 2y = 16) \;\land\; \neg(x > y))$$

Therefore:

$$\boxed{\neg \forall x, y \in D \, ((x \in \mathbb{R} \land y \in \mathbb{Z}) \to x > y)}$$

### 5. Example 5

Let the domain:
$$D = \{\langle x,y \rangle \in \mathbb{Z}^2\}$$

Evaluate:
$$\forall \langle x,y \rangle \in D \;(\text{even}(x) \leftrightarrow \text{even}(y))$$

However, we can find a counterexample:

$$
\exists x \exists y \;\big((\langle x, y \rangle \in \mathbb{Z}^2) \;\land\; x = 4 \;\land\; y = 3 \;\land\; \text{even}(x) \;\land\; \neg\text{even}(y) \;\land\; \neg(\text{even}(x) \leftrightarrow \text{even}(y))\big)
$$

Therefore:

$$\boxed{\neg \forall \langle x,y \rangle \in D \;(\text{even}(x) \leftrightarrow \text{even}(y))}$$

Note that other counterexamples include $\langle 2,5 \rangle$, $\langle 7,8 \rangle$, and any pair where one number is even and the other is odd.
