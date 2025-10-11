# Ven Diagram

One illustrative or intuitive way to represent whether a formula is valid or not is by using a Venn diagram. In this case, Venn diagrams can be used to represent the validity of syllogisms and propositions. However, for this chapter, we will only study Venn diagrams for propositions.

### 1. Ven Diagram for Conjunction

A Venn diagram for conjunction is used to show the overlap between sets $A$ and $B$, which means both $A$ and $B$ are true. The overlapping area represents:

$$
A \wedge B
$$

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Ven Dagram/Ven_Picture/Conjunction.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 1: Illustration of Conjunction
    </div>
</div>

### 2. Venn Diagram for Disjunction

A Venn diagram for disjunction is used to show the total area covered by sets $A$ and $B$, including both individual and overlapping parts. This represents $A \vee B$, meaning either $A$, $B$, or both are true.

$$
A \vee B
$$

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Ven Dagram/Ven_Picture/Disjunction.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 2: Illustration of Disjunction
    </div>
</div>

### 3. Ven Diagram for Negation

A Venn diagram for negation is used to show the area outside of circle $A$, meaning everything not in $A$. This represents that $A$ is false.

$$
\neg A
$$

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Ven Dagram/Ven_Picture/Negation.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 3: Illustration of Negation
    </div>
</div>

### 4. Venn Diagram for Implication

A Venn diagram for implication is used to show that if $A$ is true, then $B$ must also be true. Visually, this means the part of $A$ that is not in $B$ is excluded, so $A$ is entirely inside $B$, or the area where $A$ is outside $B$ is empty.

$$
A \to B
$$

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Ven Dagram/Ven_Picture/Implication.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 4: Illustration of Implication
    </div>
</div>

Moreover, that with equivalent formulas we can also show the ilustartion with the Ven Diagram. For example:

### 5. More example

Example 1.

We can also represent equivalent formulas with Venn diagrams. For example, by De Morgan’s Law: the Venn diagram for $\neg (P \wedge Q)$ shows the area outside the overlap of $P$ and $Q$. It includes everything except the region where both $P$ and $Q$ are true.

$$
\neg (P \wedge Q) \;\;\equiv\;\; (\neg P) \vee (\neg Q)
$$

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Ven Dagram/Ven_Picture/De Morgans.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 5: Illustration of De Morgan’s Law
    </div>
</div>

Example 2.

The Venn diagram for $\neg P \wedge Q$ shows the area where $Q$ is true but $P$ is false. It includes the part inside $Q$ but outside $P$.

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Ven Dagram/Ven_Picture/Not P and Q.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 6: Illustration of $\neg P \wedge Q$
    </div>
</div>
