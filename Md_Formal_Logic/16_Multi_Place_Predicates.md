<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;">Multi Place Predicates</h1>
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

As we have seen in the previous chapter, a formula like this is called a *One-Place*:

$$\forall x((A(x) \rightarrow B(x)))$$

However, not every mathematical statement deals with only one variable and predicate. That’s why we use *Multi-Place Predicates*. With multi-place predicates, we can create more expressive formulas. For example:

### 1. Two-Place Predicates

$$R(x,y)$$

Expresses a relation between two objects.

1. If there exists a number greater than $x$, then there exists a number greater than $x+1$
 $$\forall x \, (\exists y \, G(y,x) \rightarrow \exists z \, G(z,x+1))$$

2. If there exists a number $y$ equal to $x$, then $x$ equals $y$ 
 $$\forall x \, (\exists y \, E(x,y) \rightarrow E(y,x))$$

3. If $x=y$ and there exists $z$ such that $y=z$, then $x=z$ 
 $$\forall x \forall y \, ((E(x,y) \land \exists z \, E(y,z)) \rightarrow \exists z \, E(x,z))$$

4. If $x$ divides $y$, and there exists $z$ divisible by $y$, then $x$ divides $z$
$$\forall x \forall y \, (D(x,y) \land \exists z \, D(y,z) \rightarrow \exists z \, D(x,z))$$

### 2. Three-Place Predicates

$$R(x,y,z)$$

Expresses a relation among three objects.

1. For every number $x$, there exists a number $y$ such that $x$ is less than $y$.
$$\forall x \, \exists y \, L(x,y)$$

2. For all numbers $p$, if $p$ is prime, then there exists a number $q$ such that $q$ = $p + 2$.
$$\forall p \, (\mathbb{P}(p) \rightarrow \exists q \, (q = p+2))$$

3. For all numbers $n$, if $n$ is even, then there exists a number $m$ such that $m = n/2$.
$$\forall n \, (\text{Even}(n) \rightarrow \exists m \, (m = n/2))$$

4. For all $x$, if $x$ is a natural number, then there exists a $y$ in the integers such that $x$ is not equal to $y$.
$$\forall x \, (x \in \mathbb{N} \rightarrow \exists y \, (y \in \mathbb{Z} \land x \neq y))$$

### 3. Four-Place Predicates

$$Q(w,x,y,z)$$

Expresses a relation among four objects.

1. For every $a$ and $b$, there exists a $c$ such that $a+b+c$ is even
$$\forall a \forall b \, \exists c \exists d \, (Q(a,b,c,d) \land \text{Even}(d))$$

2. If $a,b,c$ are positive, then there exists $d>0$ such that $a+b+c=d$
$$\forall a \forall b \forall c \, ((a>0 \land b>0 \land c>0) \rightarrow \exists d \, Q(a,b,c,d) \land d>0)$$

3. For every $x,y$, there exists $z$ such that $x \times y + z$ is even
$$\forall x \forall y \, \exists z \exists w \, (P(x,y,z,w) \land \text{Even}(w))$$

4. If $x,y,z>0$, then there exists $w>0$ such that $x \times y + z = w$
$$\forall x \forall y \forall z \, ((x>0 \land y>0 \land z>0) \rightarrow \exists w \, P(x,y,z,w) \land w>0)$$
