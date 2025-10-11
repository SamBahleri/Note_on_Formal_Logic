<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;">Properties of Relations</h1>
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

Let $R \subseteq A^2$ be a binary relation on a set $A$:

1. Reflexivity: 
$$R \subseteq A^2 \leftrightarrow \forall x \, (A(x) \to xRx)$$

2. Irreflexivity: 
$$R \subseteq A^2 \leftrightarrow \forall x \, (A(x) \to \neg (xRx))$$

3. Asymmetry:
$$R \subseteq A^2 \leftrightarrow \forall x \forall y \, (A(x,y) \to (xRy \to \neg (yRx)))$$

4. Symmetry:
$$R \subseteq A^2 \leftrightarrow \forall x \forall y \, (A(x,y) \to (xRy \to yRx))$$

5. Antisymmetry:
$$R \subseteq A^2 \leftrightarrow \forall x \forall y \, (A(x,y) \to ((xRy \land yRx) \to x = y))$$

6. Transitivity:
$$R \subseteq A^2 \leftrightarrow \forall x \forall y \forall z \, (A(x,y,z) \to ((xRy \land yRz) \to xRz))$$

7. Connectivity:
$$R \subseteq A^2 \leftrightarrow \forall x \forall y \, (A(x,y) \to (x \neq y \to (xRy \lor yRx)))$$

## 1. Reflexivity

$$\forall x \in A, \ xRx$$

Example:

The relation $\leq$ on $\mathbb{R}$ is reflexive because $3 \leq 3$. Likewise, the subset relation $\subseteq$ is reflexive: $\{1\} \subseteq \{1\}$. In both cases, every element is related to itself.

## 2. Irreflexivity

$$\forall x \in A, \ \neg(xRx)$$

Example:

The relation $<$ on $\mathbb{N}$ is irreflexive because no number is less than itself: $5 < 5$ is false, so $\neg(5<5)$.

## 3. Asymmetry

$$\forall x,y \in A,\ xRy \to \neg(yRx)$$

Example:

The relation $<$ on $\mathbb{N}$ is asymmetric because $2 < 3$, but $3 < 2$ is false. There is no pair such that both $xRy$ and $yRx$ hold. Therefore, $<$ is asymmetric. Any asymmetric relation is automatically irreflexive.

## 4. Symmetry

$$\forall x,y \in A, \ xRy \to yRx$$

Example:

Let

$$A = \{1,2,3\} \quad \text{and} \quad R = \{1R2, 2R1, 2R3, 3R2\}$$

This relation is symmetric because:

$$1R2  \quad \text{and} \quad 2R1$$

$$2R3 \quad \text{and} \quad 3R2$$

Every pair has its mirror image in the relation. Therefore, $R$ is symmetric.

## 5. Antisymmetry

$$\forall x,y \in A,\ (xRy \land yRx) \to x = y$$

Example 1 (on $\mathbb{N}$):  

Let $R = \leq$. If $x \leq y$ and $y \leq x$, then $x = y$. Therefore, $\leq$ is antisymmetric.

## 6. Transitivity

$$\forall x,y,z \in A,\ (xRy \land yRz) \to xRz$$

Example:  

The relation $<$ on $\mathbb{N}$ is transitive:  

$$2 < 4 \land 4 < 5 \to 2 < 5$$

## 7. Connectivity

$$\forall x,y \in A,\ x \neq y \to (xRy \lor yRx)$$

Example 1 (on $\mathbb{N}$):  

The relation $\leq$ is connected because for any distinct $x,y$, either $x \leq y$ or $y \leq x$.

Example 2 (on $<$):  

The relation $<$ on $\mathbb{N}$ is connected because for $x \ne y$, either $x < y$ or $y < x$.

Importantly, in evaluating the relations, it is also necessary to learn the order. Specifically, If $L(x,y)$ is a binary predicate, then $L(a,b)$ and $L(b,a)$ are not the same formula unless the semantics of $L$ itself makes them equivalent.

Example:

If $L(x,y)$ means “$x$ loves $y$”, then:

− $L(a,b) =$ “$a$ loves $b$”

− $L(b,a) =$ “$b$ loves $a$”

These are logically distinct, unless we assume love is symmetric. So we usually use this bracket symbol to stress the order $\langle a, b \rangle$. Nevertheless, in general, for FOL, we can still use (,), but keep in mind that the order matters.
