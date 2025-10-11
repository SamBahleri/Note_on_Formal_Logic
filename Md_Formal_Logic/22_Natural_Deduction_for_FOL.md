# Natural Deduction for FOL

The way we perform deductions in first-order logic (FOL) is essentially similar to propositional logic (PL), for example, we use rules like Modus Ponens ($MP$) and Modus Tollens ($MT$). However, in FOL the process is generally longer because we must also handle quantifiers and carefully substitute variables before applying these rules.

### 1. Universal elimination ($\forall E$)

<div class="image-container">
    <img src="/FOL_ND/1.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 1:  Universal elimination
    </div>
</div>

Universal elimination allows us to instantiate a universally quantified statement with any specific term. If something is true for all objects in the domain, then it must be true for any particular object we choose.

Given: $$\forall x\, P(x)$$
We can conclude: $$P(a)  \quad \text{for any term $a$ } $$

The rule can be written as:
$$\frac{\forall x\, P(x)}{\therefore P(a)}$$

### 2. Existential Introduction ($\exists I$)

<div class="image-container">
    <img src="/FOL_ND/2.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 2: Existential Introduction
    </div>
</div>

Given: $$P(a)$$
We can conclude: $$\exists x\, P(x)$$

The rule can be written as:
$$\frac{P(a)}{\therefore \exists x\, P(x)}$$

### 3. Universal Introduction ($\forall I$)

<div class="image-container">
    <img src="/FOL_ND/3.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 3: Universal Introduction
    </div>
</div>

Universal introduction allows us to conclude a universal statement if we can prove something about an arbitrary object. The key constraint is that the object must be completely arbitrary, it cannot depend on any specific assumptions about particular objects.

From a proof that establishes $P(a)$ where $a$ is arbitrary, we can conclude: $$\forall x\, P(x)$$

The rule can be written as:
$$\frac{\text{[Arbitrary } a\text{]} \quad P(a)}{\therefore \forall x\, P(x)}$$

### 4. Existential elimination ($\exists E$)

<div class="image-container">
    <img src="/FOL_ND/4.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 4:  Existential elimination
    </div>
</div>

Existential elimination allows us to use an existential statement in a proof. Since we know something exists with a certain property, we can temporarily assume we have such an object (giving it a fresh name) and see what follows.

Given: $$\exists x\, P(x)$$

We can assume $P(a)$ for a fresh name $a$, derive some conclusion $Q$, and then conclude $Q$ without the assumption.

The rule can be written as:
$$\frac{\exists x\, P(x) \quad \text{[Assume } P(a)\text{]} \quad Q}{\therefore Q}$$

### 5. Identity Introduction ($=I$)

<div class="image-container">
    <img src="/FOL_ND/5.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 5:  Identity Introduction
    </div>
</div>

Identity introduction states that every object is identical to itself. This is a logical truth that requires no premises.

We can always conclude: $$a = a \quad \text{for any term} \quad a$$

The rule can be written as:
$$\frac{}{\therefore a = a}$$

This reflects the reflexive property of identity.

### 5. Identity elimination ($=E$)
<div class="image-container">
    <img src="/FOL_ND/6.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 6:  Identity elimination
    </div>
</div>

Identity elimination, also known as Leibniz's Law, states that identical objects have identical properties. If two terms refer to the same object, we can substitute one for the other in any context.

Given: $$a = b \quad \text{and} \quad P(a)$$
We can conclude: $$P(b)$$

The rule can be written as:
$$\frac{a = b \quad P(a)}{\therefore P(b)}$$

### 6. Conversion of Quantifiers (CQ) Rules

Recall the Quantifier Equivalences, these derived rules show the relationship between quantifiers and negation:

1. CQ1: $$\forall x\, \neg P(x) \leftrightarrow \neg \exists x\, P(x)$$
   *Everything is not P* is equivalent to *Nothing is P*

2. CQ2: $$\neg \exists x\, P(x) \leftrightarrow \forall x\, \neg P(x)$$
   *Nothing is P* is equivalent to *Everything is not P*

3. CQ3: $$\exists x\, \neg P(x) \leftrightarrow \neg \forall x\, P(x)$$
   *Something is not P* is equivalent to *Not everything is P*

4. CQ4: $$\neg \forall x\, P(x) \leftrightarrow \exists x\, \neg P(x)$$
   *Not everything is P* is equivalent to *Something is not P*
