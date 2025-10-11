<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;"> First Order Logic </h1>

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

/* Tables */
table {
margin: 2rem auto; /* center the table */
border-collapse: collapse;
width: auto; /* shrink to content instead of full width */
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

Basically, reasoning rules such as Double Negation ($DN$), Modus Ponens ($MP$), and Reductio ad Absurdum ($RAA$) are the most basic forms of reasoning. However, as we have learned, these three rules more often only work on logical patterns between statements. In other words, although deductively valid, their application is not yet complete enough to capture deeper mathematical structures.

As an example, consider the following statements:

− $p$: 2 is prime

− $q$: 2 $\in \mathbb{N}$

If we convert this into symbolic form, we get:

$$p \land q$$

However, it should be noted that $p$ and $q$ here are merely representations of complete sentences in natural language. This symbolization has not yet touched the predicate level inherent in the number 2, namely the property of being prime and its membership in the set $\mathbb{N}$. In other words, propositional logic only “packages statements”, but has not yet “dissected” the mathematical content of the statement itself. Therefore, a richer framework is needed to capture such expressions. This is where First-Order Logic (FOL) becomes crucial, as it allows us to express properties, relations, and quantification over mathematical objects more precisely.

## 1. Sentence of FOL

Normally, there are six kinds of symbols in FOL, and most of them are similar to those in propositional logic:

1. Constant symbols
 $$a, b, c, \dots, r, a_1, b_{224}, h_7, m_{32}, \dots$$

2. Variable symbols
 $$s, t, u, v, w, x, y, z, x_1, y_1, z_1, x_2, \dots$$

3. Function symbols
 $$f, g, h, f_1, g_2, h_{37}, \dots$$

4. Predicate symbols
 $$A, B, C, \dots, Z, A_1, B_1, Z_1, A_2, A_{25}, J_{375}, \dots, =$$

5. Logical connectives
 $$\lnot, \land, \lor, \to, \leftrightarrow$$

6. Brackets
 $$( \ , \ )$$

7. Quantifiers
 $$\forall, \exists$$

## 2. Terms and formulas

1. Every atomic formula is a formula.
2. If $a$ and $b$ are formulas, then so are:
    1. $\lnot a$
    2. $(a \land b)$
    3. $(a \lor b)$
    4. $(a \to b)$
    5. $(a \leftrightarrow b)$
3. If $a$ is a formula and $x$ is a variable, then:
    1. $\forall x \, a$
    2. $\exists x \, a$

## 3. Bracketing Conventions in FOL

1. Outer parentheses may be omitted.

  $$
  a \land b \quad \text{instead of} \quad (a \land b)
  $$

2. Negation binds most tightly.

  $$
  \lnot a \lor b \quad \text{means} \quad (\lnot a) \lor b
  $$

3. Quantifiers extend as far to the right as possible.

  $$
  \forall x \, a \lor b \quad \text{means} \quad (\forall x \, a) \lor b
  $$

4. Other connectives associate to the right unless parentheses indicate otherwise.

  $$
  a \lor b \lor c \quad \text{means} \quad a \lor (b \lor c)
  $$

## 4. Superscripts on Predicates in FOL

1. Predicate symbols may be written with superscripts to indicate their arity.

  $$
  P^1 \text{ (unary)}, \quad Q^2 \text{ (binary)}, \quad R^3 \text{ (ternary)}
  $$

2. In general, if $P^n$ is an $n$-place predicate and $t_1, \dots, t_n$ are terms, then

  $$P^n(t_1, \dots, t_n) \text{ is an atomic formula.}$$

## 5. Name

Names, in general, function to indicate both the existence of an entity and serve as a reference for a particular object or place. For example, the word “Gottlob Frege” refers specifically to an individual, a great logician who was instrumental in the development of predicate logic. However, it must be recognized that if someone has never heard the name “Gottlob Frege” before, they may not know who is being referred to. In fact, that person might even imagine that “Gottlob Frege” is not the name of a human being, but merely a term or particular object. Such conditions are known in philosophy of language as a problem inherent in proper names, namely the potential ambiguity in reference.

Within the framework of FOL, such ambiguity cannot be tolerated. The reason is simple, when we engage in formal reasoning, we require that the expressions used be clear, syntactically valid, and also sound in meaning. Therefore, naming in FOL must have definite reference and leave no room for double interpretation. In FOL, constant symbols usually function like proper names, pointing specifically to an object within the domain. For example:

1. Constant $a$ refers to object $2$ in $\mathbb{N}$.

2. Constant $b$ refers to object $-5$ in $\mathbb{Z}$.

So when we write the predicate $Prime(a)$, it must be understood definitively as “2 is a prime number.” There can be no ambiguity about whether $a$ refers to the number 2, to a person named “Gottlob Frege” or even to a chair, because in FOL, the interpretation of every symbol must be clear within the established domain.

## 6. Predicate

In everyday language, a predicate is the part of a statement that provides information or describes the subject. For example, in the sentence *Snow is white* the phrase “is white” is the predicate.

Consider the following example:

$ \text{Premise 1: All humans are mortal.}$

$ \text{Premise 2: Socrates is a human.}$

$ \text{Conclusion: Therefore, Socrates is mortal}$

As we can see, expressions such as *“are mortal”* and *“is a human”* are predicates. Through such structures, predicate logic enables us to express relationships and properties of objects in greater depth than standard propositional logic. Moreover, it is important to understand that a predicate like *“mortal”* is not a standalone proposition but a component of one. A predicate can be thought of as a framework or function with an empty slot waiting to be filled by a subject. For example:

−$Mortal(\dots)$

This structure may feel counterintuitive, since we are accustomed to complete sentences in natural language. However, there are historical and logical reasons why this functional form is preferred in formal logic.

Following the example above, if we fill the blank with *Socrates*, we obtain:

−$Mortal(Socrates)$

This indicates that *“Socrates”* is placed in the subject position of the predicate *“mortal”*, forming a complete proposition. For simplicity and efficiency, logicians often replace predicate names with a single capital letter. Thus, $Mortal(Socrates)$ is simplified to:

−$M(Socrates)$ , where $M$ represents the predicate *“mortal.”*

We can simplify even further by representing the name *“Socrates”* with the constant $S$. Therefore, the whole expression becomes:

−$M(S)$

Furthermore, to express *“Socrates is human and mortal”*, we can combine the two predicates into a single expression:

− $H(S) \land M(S)$

Thus, the expression $H(S) \land M(S)$ states that Socrates satisfies both predicates: he is a human and he is mortal. Accordingly, we can also represent general statements using formulas with *free variables*. The idea is that the variable serves as a placeholder, or a “blank,” that can later be filled by any element from the domain of discourse. For example:

− $P(x)$

− $O(x)$

## 7. Quantifiers

Shortly speaking, when discussing predicate logic, one immediately thinks of Gottlob Frege (1848–1925). Frege introduced the concept of quantifiers, namely $\forall$ and $\exists$. These concepts were later popularized in the early 20th century by Bertrand Russell and Alfred North Whitehead through their seminal work *Principia Mathematica*.

The use of these symbols is essential to represent not only a single variable but also many variables. For example:

− Everyone is happy

In this case, we cannot represent the statement merely as $H(e)$, as we did in the Socrates” example. Instead, we represent it as:

$$\forall x \, H(x)$$

In this case, we can represent anything with the predicate *Happy*. The variable acts as a placeholder, so whatever we choose from the domain can be tested against the predicate. This shows that the predicate *Happy* is not tied to a single individual but can be applied universally to any object in the chosen domain of discourse.

Similarly, consider the example:

$$\text{Someone is unique}$$

We can represent this statement using the existential quantifier as follows:

$$\exists x \, U(x)$$

Here:
− $\exists x$ intuitively means *“there exists at least one x”* in the domain.

− $U(x)$ states that this $x$ has the property of being unique.

Thus, the formula $\exists x \, U(x)$ expresses that there is at least one object in the domain such that the predicate *Unique* applies to it.

$$\text{Everyone loves someone}$$

$$\forall x \exists y \, L(x,y)$$

This formula uses two variables: $x$ represents the lover and $y$ represents the beloved. The formula states that for every person $x$ in the domain, there exists some person $y$ such that $x$ loves $y$.

$$\text{Someone is loved by everyone}$$

$$\exists y \forall x \, L(x,y)$$

This formula states that there exists a person $y$ such that for all persons $x$, $x$ loves $y$, meaning there is one person who is universally loved.

$$\text{If someone is a teacher, then everyone respects them}$$

$$\exists x (T(x) \land \forall y \, R(y,x))$$

This formula combines both quantifiers with a conditional structure. It states that there exists a person $x$ who is a teacher, and for all persons $y$, $y$ respects $x$.

$$\text{Everyone who teaches logic is respected by all students}$$

$$\forall x ((T(x) \land L(x)) \rightarrow \forall y (S(y) \rightarrow R(y,x)))$$

This more complex formula involves multiple predicates, $T(x)$ means “$x$ teaches”, $L(x)$ means “$x$ teaches logic”, $S(y)$ means “$y$ is a student”, and $R(y,x)$ means “$y$ respects $x$”. The formula demonstrates how multiple variables can interact within nested quantifier scopes.

## 8. Domains

It is also important to comprehend the domain of our reasoning in predicate logic. The critical point arises when we begin to express more complex statements, we must be precise about how variables are used within predicates.

Consider the formula:

$$\forall x \, H(x)$$

which we might translate as “Everyone is happy.” But who exactly counts as “everyone”? In everyday English, we do not usually mean literally every person who has ever lived or ever will live. We typically mean something more limited: everyone in this building, everyone in a class, everyone on a team, and so on. Predicate logic removes this ambiguity by requiring us to specify a domain of discourse. The domain is the set of objects under discussion.

For example, suppose we set our symbolization key as follows:

− Domain: people in Finland

− $H(x)$: $x$ is happy

Now the quantifiers range only over that domain.

− $\forall x \, H(x)$ means “Every person in Finland is happy.”

− $\exists x \, H(x)$ means “Some person in Finland is happy.”

In FOL, the domain must contain at least one member, and each name must refer to exactly one object in that domain. So if $S$ names Sam, then from $H(S)$ (“Sam is happy”) we can infer $\exists x \, H(x)$ (“Someone is happy”).

The choice of domain is crucial. Suppose we instead use this symbolization key:

− Domain: the Eiffel Tower

− $P(x)$: $x$ is in Paris

Then $\forall x \, P(x)$ would translate as “Everything is in Paris.” But since the domain contains only the Eiffel Tower, what the sentence really says is simply: “The Eiffel Tower is in Paris.”

Another example, suppose we want to say:

$$\text{There is exactly one king in the palace.}$$

If we only write:

$$\exists x \, King(x)$$

this means *“there exists at least one $x$ such that $x$ is a king.”* But it does not prevent the possibility of there being two or more kings. To capture the idea of uniqueness, we need to express that there is *one and only one*. This is often written with the uniqueness quantifier $\exists!$

$$\exists! x \, King(x)$$

Alternatively, we can express uniqueness using standard quantifiers:

$$\exists x (King(x) \land \forall y (King(y) \rightarrow x = y))$$

This formula states: “There exists an $x$ such that $x$ is a king, and for all $y$, if $y$ is a king, then $x$ equals $y$”, ensuring there is exactly one king.

## 9. Quantifiers and Scope

When we introduce quantifiers into formal logic, understanding their scope becomes crucial for accurate translation and interpretation. The scope of a quantifier determines which variables it binds and how far its influence extends in a formula. 

1. Example 1:
    $$\text{If anyone is a teacher, they are respected}$$
    $$
    \color{black}{\overbrace{\color{black}\forall x \, (T(x) \to R(x))}^{\color{black}\text{Scope of } \forall x}}
    $$

    The universal quantifier scopes over the conditional, creating a universal generalization. This statement holds vacuously true in domains without teachers. *All teachers are respected* yields the same logical form.

2. Example 2:

    $$\text{Every professor knows a student who failed}$$

    $$
    {\color{black}\overbrace{\color{black}\forall y \, \Big( \text{Professor}(y) \rightarrow
    {\color{black}\overbrace{\color{black}\exists x \, (\text{Student}(x) \wedge \text{Failed}(x) \wedge \text{Knows}(y,x))}^{\color{black}\text{Scope of } \exists x}} \Big)}^{\color{black}\text{Scope of } \forall y}}
    $$

3. Example 3:

    $$\text{Every student has submitted some assignment to each professor}$$

    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big( \text{Student}(x) \rightarrow
    {\color{black}\overbrace{\color{black}\forall z \, (\text{Professor}(z) \rightarrow 
    {\color{black}\overbrace{\color{black}\exists y \, (\text{Assignment}(y) \wedge \text{Submitted}(x,y,z))}^{\color{black}\text{Scope of } \exists y}})}^{\color{black}\text{Scope of } \forall z}} \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

## 10. The Order of Quantifiers

1. Example 1:

    Consider the sentence *Everyone admires some Logician*. This is ambiguous and can be represented in two different ways:

    Interpretation 1: For every person $x$, there exists some Logician $y$ such that $x$ admires $y$:

    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big(
    {\color{black}\overbrace{\color{black}\exists y \, (Person(x) \wedge Logician(y) \wedge Admires(x,y))}^{\color{black}\text{Scope of } \exists y}}
    \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* Everyone may admire different Logician.

    Interpretation 2: There exists some particular Logician $y$ such that every person $x$ admires $y$:

    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    \Big(
    \text{Logician}(y) \wedge
    {\color{black}\overbrace{\color{black}\forall x \,
    ( \text{Person}(x) \wedge \text{Admires}(x,y) )
    }^{\color{black}\text{Scope of } \forall x}}
    \Big)
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* There's one particular Logician who everyone admires.

2. Example 2:

    Consider the sentence *Every student passed some exam*. This has two distinct interpretations:

    Interpretation 1: For each student, there exists at least one exam they passed
    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big(
    \text{Student}(x) \rightarrow
    {\color{black}\overbrace{\color{black}\exists y \, (\text{Exam}(y) \wedge \text{Passed}(x,y))}^{\color{black}\text{Scope of } \exists y}}
    \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* Each student passed at least one exam (possibly different exams).

    Interpretation 2: There exists one particular exam that every student passed
    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    \Big(
    \text{Exam}(y) \wedge
    {\color{black}\overbrace{\color{black}\forall x \, 
    ( \text{Student}(x) \rightarrow \text{Passed}(x,y) )
    }^{\color{black}\text{Scope of } \forall x}}
    \Big)
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* There's one specific exam that all students passed.

    Consider the sentence *Every patient has some symptom*:

    Interpretation 1: Each patient exhibits at least one symptom
    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big(
    \text{Patient}(x) \rightarrow
    {\color{black}\overbrace{\color{black}\exists y \, (\text{Symptom}(y) \wedge \text{Has}(x,y))}^{\color{black}\text{Scope of } \exists y}}
    \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* Every patient shows some symptoms (different symptoms for different patients).

    Interpretation 2: There's one symptom that all patients have
    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    \Big(
    \text{Symptom}(y) \wedge
    {\color{black}\overbrace{\color{black}\forall x \, 
    ( \text{Patient}(x) \rightarrow \text{Has}(x,y) )
    }^{\color{black}\text{Scope of } \forall x}}
    \Big)
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* There's a common symptom shablack by all patients.

3. Example 3:

    Consider the sentence *Every company hiblack some consultant*:

    Interpretation 1: Each company hiblack at least one consultant
    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big( 
    \text{Company}(x) \rightarrow
    {\color{black}\overbrace{\color{black}\exists y \, (\text{Consultant}(y) \wedge \text{Hiblack}(x,y))}^{\color{black}\text{Scope of } \exists y}} 
    \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* Each company hiblack consultants (possibly different ones).

    Interpretation 2: There's one consultant hiblack by all companies
    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    \Big(
    \text{Consultant}(y) \wedge
    {\color{black}\overbrace{\color{black}\forall x \, 
    ( \text{Company}(x) \rightarrow \text{Hiblack}(x,y) )
    }^{\color{black}\text{Scope of } \forall x}}
    \Big)
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* One super-consultant was hiblack by every company.

    Consider the sentence *For every number, there exists a larger number*:

    Interpretation 1: For each number, we can find a larger one
    $$
    {\color{black}\overbrace{\color{black}\forall x \,
    {\color{black}\overbrace{\color{black}\exists y \, (x < y)}^{\color{black}\text{Scope of } \exists y}} 
    }^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* There's no largest number (true statement).

    Interpretation 2: There exists one number larger than all numbers
    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    {\color{black}\overbrace{\color{black}\forall x \, (x < y)}^{\color{black}\text{Scope of } \forall x}}
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* There's a supremely large number (false statement).

4. Example 4:

    Consider the sentence *Everyone trusts someone*:

    Interpretation 1: Each person trusts at least one person
    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big(
    \text{Person}(x) \rightarrow
    {\color{black}\overbrace{\color{black}\exists y \, (\text{Person}(y) \wedge \text{Trusts}(x,y))}^{\color{black}\text{Scope of } \exists y}}
    \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* Nobody is completely distrustful; everyone trusts someone.

    Interpretation 2: There's one person trusted by everyone
    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    \Big(
    \text{Person}(y) \wedge
    {\color{black}\overbrace{\color{black}\forall x \, 
    ( \text{Person}(x) \rightarrow \text{Trusts}(x,y) )
    }^{\color{black}\text{Scope of } \forall x}}
    \Big)
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* There's a universally trusted person.

5. Example 5:

    Consider the sentence *Every device connects to some network*:

    Interpretation 1: Each device connects to at least one network
    $$
    {\color{black}\overbrace{\color{black}\forall x \, \Big(
    \text{Device}(x) \rightarrow
    {\color{black}\overbrace{\color{black}\exists y \, (\text{Network}(y) \wedge \text{Connects}(x,y))}^{\color{black}\text{Scope of } \exists y}}
    \Big)}^{\color{black}\text{Scope of } \forall x}}
    $$

    *Interpretation:* All devices have network connectivity (possibly to different networks).

    Interpretation 2: There's one network that all devices connect to
    $$
    {\color{black}\overbrace{\color{black}\exists y \,
    \Big(
    \text{Network}(y) \wedge
    {\color{black}\overbrace{\color{black}\forall x \,
    ( \text{Device}(x) \rightarrow \text{Connects}(x,y) )
    }^{\color{black}\text{Scope of } \forall x}}
    \Big)
    }^{\color{black}\text{Scope of } \exists y}}
    $$

    *Interpretation:* There's a universal network that connects all devices.

These examples demonstrate how the *quantifier shift fallacy* can dramatically alter meaning. The pattern $\forall x \exists y$ (distributive) versus $\exists y \forall x$ (collective) represents fundamentally different logical relationships, making quantifier order crucial for precise logical reasoning.

## 11. Free and Bound Variables

In the rules of predicate logic, we must also understand the concepts of free variables and bound variables. In short, a free variable is an object being referred to but is not within the scope of a universal or existential quantifier. Whereas a bound variable is an object that is expressed within the scope of a quantifier, either universal or existential. Understanding this distinction is essential for correctly interpreting logical formulas and determining whether a formula is closed (has no free variables) or open (contains free variables).

1. Free variable

    Consider the formula:
    $$
    \forall x \, \Big(
    P(x) \wedge 
    {\color{black}\overbrace{\color{black}Q(y)}^{\color{black}\text{Free}}}
    \Big)
    $$

    In this formula, $x$ is bound by the universal quantifier $\forall x$, but $y$ is free because it is not within the scope of any quantifier. The truth of this formula depends on the value of y, while x is quantified over all possible values.

2. Bound variable

    Consider the formula:

    $$
    {\color{black}\overbrace{\color{black}\exists x\,
    \big(
    P(x) \wedge Q(x)
    \big)
    }^{\color{black}\text{Scope of } \exists x}}
    $$

    In this formula, $x$ is bound by the existential quantifier $\exists x$. The truth of the formula does not depend on any external value of $x$, because it is fully specified within the scope of the quantifier.

3. Mixed free and bound variables

    Consider the formula:
    $$
    \forall x \, \Big(
    P(x, {\color{black}\overbrace{\color{black}y}^{\color{black}\text{Free}}}) \rightarrow 
    \exists z \, 
    {\color{black}\overbrace{\color{black}Q(x, z)}^{\color{black}\text{Both bound}}}
    \Big)
    $$

    Here:

    − $x$ is bound by $\forall x$

    − $z$ is bound by $\exists z$

    − $y$ is free (appears in $P(x,y)$ but isn't quantified)

    The truth value depends on what $y$ represents, while $x$ and $z$ are internally determined.

4. Nested quantifiers with name collision

    Consider the formula:
    $$
    \forall x \, \Big(
    P(x) \rightarrow 
    {\color{black}\overbrace{\color{black}\exists x \, R(x, y)}^{\color{black}\text{Inner } x \text{ bound}}}
    \Big)
    $$

    Here we have two different variables both named $x$:

    − The outer $x$ is bound by $\forall x$ in $P(x)$

    − The inner $x$ is bound by $\exists x$ in $R(x,y)$ 

    − $y$ is free throughout

    The inner quantifier “shadows the outer one within its scope.

5. Multiple free variables

    Consider the formula:
    $$
    {\color{black}\overbrace{\color{black}P(a, b)}^{\color{black}\text{Both free}}} \wedge 
    \forall x \,
    {\color{black}\overbrace{\color{black}Q(x, c)}^{\color{black}c \text{ is free}}}
    $$

    Here:

    − $a$, $b$, and $c$ are all free variables

    − $x$ is bound by $\forall x$

    The truth depends on the specific values assigned to $a$, $b$, and $c$.

6. Complex nesting

    Consider the formula:
    $$
    \exists x \, \forall y \, \Big(
    {\color{black}\overbrace{\color{black}P(x, y)}^{\color{black}\text{Both bound}}} \rightarrow
    \exists z \,
    \big(
    {\color{black}\overbrace{\color{black}Q(x, z)}^{\color{black}\text{Both bound}}} \wedge
    {\color{black}\overbrace{\color{black}R(w)}^{\color{black}w \text{ free}}}
    \big)
    \Big)
    $$

    Here:

    − $x$ is bound by $\exists x$ (outermost)

    − $y$ is bound by $\forall y$ 

    − $z$ is bound by the inner $\exists z$

    − $w$ is free (not quantified anywhere)

7. No quantifiers (all free)

    Consider the formula:
    $$
    {\color{black}\overbrace{\color{black}P(a) \wedge Q(b, c) \rightarrow R(a, d)}^{\color{black}\text{All variables free}}}
    $$

    Since there are no quantifiers, all variables $a$, $b$, $c$, and $d$ are free. The truth value depends entirely on the interpretation of these variables.

8. Sequential quantifiers

    Consider the formula:
    $$
    \forall x \, \exists y \, \forall z \, 
    {\color{black}\overbrace{\color{black}P(x, y, z)}^{\color{black}\text{All bound}}} \wedge 
    {\color{black}\overbrace{\color{black}Q(w)}^{\color{black}w \text{ free}}}
    $$

    Here:

    − $x$ is bound by $\forall x$

    − $y$ is bound by $\exists y$

    − $z$ is bound by $\forall z$

    − $w$ is free

    The quantifiers create a chain: “for all $x$, there exists a $y$, such that for all $z$...”

9. Partial binding

    Consider the formula:
    $$
    \exists x \,
    \Big(
    {\color{black}\overbrace{\color{black}P(x)}^{\color{black}\text{Bound}}} \wedge 
    {\color{black}\overbrace{\color{black}Q(x, y)}^{\color{black}x \text{ bound, } y \text{ free}}}
    \Big) \rightarrow
    {\color{black}\overbrace{\color{black}R(y, z)}^{\color{black}\text{Both free}}}
    $$

    Here:

    − $x$ is bound by $\exists x$ within the antecedent

    − $y$ appears both bound (in the scope of $\exists x$) and free (in $R(y,z)$)

    − $z$ is free throughout

    This shows how the same variable name can have different binding status in different parts of a formula.

## 12. Quantifier Equivalences

We understand that one logical symbol can often be rewritten in terms of others. In propositional logic, for instance, the implication symbol $(\rightarrow)$ can be expressed using disjunction $(\lor)$ and negation $(\lnot)$. For example:

$$
p \rightarrow q \;\;\equiv\;\; \lnot p \lor q
$$

A similar relationship exists in picate logic between the universal quantifier $(\forall)$ and the existential quantifier $(\exists)$, connected through negation:

$$
\forall x \, c(x) \;\;\equiv\;\; \lnot \exists x \, \lnot c(x)
$$

This means: *“For all $x$, $c(x)$ holds”* is equivalent to *“There does not exist an $x$ such that $c(x)$ does not hold.”*

Conversely:

$$
\exists x \, c(x) \;\;\equiv\;\; \lnot \forall x \, \lnot c(x)
$$

This means: *“There exists an $x$ such that $c(x)$ holds”* is equivalent to *“It is not the case that $c(x)$ fails for all $x$.”*

These equivalences also extend naturally to statements beginning with negation:

$$
\lnot \forall x \, c(x) \;\;\equiv\;\; \exists x \, \lnot c(x)
$$

This means: *“It is not true that $c(x)$ holds for all $x$”* is logically equivalent to saying *“There exists at least one $x$ such that $c(x)$ does not hold.”*

And similarly:

$$
\lnot \exists x \, c(x) \;\;\equiv\;\; \forall x \, \lnot c(x)
$$

This means: *“It is not true that there exists an $x$ such that $c(x)$ holds”* is logically equivalent to saying *“For every $x$, $c(x)$ does not hold.”*

## 13. Symbolizing Syllogistic Reasoning

Let’s now translate classical syllogisms into predicate logic. We’ll use the following key:

Key for predicates:
− $M(x)$: $x$ is an $M$ (middle term)
− $S(x)$: $x$ is an $S$ (subject term)
− $P(x)$: $x$ is a $P$ (predicate term)

1. Barbara (AAA)

    Form:
    − All $M$ are $P$
    − All $S$ are $M$
    − $\therefore$ All $S$ are $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow P(x))$
    − $\forall x \, (S(x) \rightarrow M(x))$
    − $\therefore$ $\forall x \, (S(x) \rightarrow P(x))$

    Everything $M$ is included in $P$. Since all $S$ fall under $M$, they too must fall under $P$.

2. Celarent (EAE)

    Form:
    − No $M$ are $P$
    − All $S$ are $M$
    − $\therefore$ No $S$ are $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\forall x \, (S(x) \rightarrow M(x))$
    − $\therefore$ $\forall x \, (S(x) \rightarrow \lnot P(x))$

    Being an $M$ rules out being a $P$. Since all $S$ are $M$, none of them can possibly be $P$.

3. Darii (AII)

    Form:
    − All $M$ are $P$
    − Some $S$ are $M$
    − $\therefore$ Some $S$ are $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow P(x))$
    − $\exists x \, (S(x) \land M(x))$
    − $\therefore$ $\exists x \, (S(x) \land P(x))$

    The universal ensures every $M$ is also $P$. Since at least one $S$ is an $M$, that same $S$ must also be a $P$.

4. Ferio (EIO)

    Form:
    − No $M$ are $P$
    − Some $S$ are $M$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\exists x \, (S(x) \land M(x))$
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    If being $M$ excludes being $P$, and some $S$ is $M$, then that same $S$ must also not be $P$.

5. Cesare (EAE)

    Form:
    − No $P$ are $M$
    − All $S$ are $M$
    − $\therefore$ No $S$ are $P$

    Symbolization:
    − $\forall x \, (P(x) \rightarrow \lnot M(x))$
    − $\forall x \, (S(x) \rightarrow M(x))$
    − $\therefore$ $\forall x \, (S(x) \rightarrow \lnot P(x))$

    If no $P$ can be an $M$, then nothing counted as $P$ overlaps with $M$. Since all $S$ are $M$, none of them can belong to $P$.

6. Camestres (AEE)

    Form:
    − All $P$ are $M$
    − No $S$ are $M$
    − $\therefore$ No $S$ are $P$

    Symbolization:
    − $\forall x \, (P(x) \rightarrow M(x))$
    − $\forall x \, (S(x) \rightarrow \lnot M(x))$
    − $\therefore$ $\forall x \, (S(x) \rightarrow \lnot P(x))$

    Everything $P$ is also $M$. But $S$ can never be $M$. So $S$ can never be $P$ either.

7. Festino (EIO)

    Form:
    − No $M$ are $P$
    − Some $S$ are $M$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\exists x \, (S(x) \land M(x))$ 
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    If $M$ excludes $P$, then any $S$ that happens to be $M$ cannot be $P$.

8. Baroco (AOO)

    Form:

    − All $M$ are $P$
    − Some $S$ are not $M$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow P(x))$
    − $\exists x \, (S(x) \land \lnot M(x))$
    − $\therefore \, \exists x \, (S(x) \land \lnot P(x))$

    Explanation:
    Every $M$ is guaranteed to be $P$. But since there are some $S$ that are outside $M$, those $S$ might fall outside $P$ as well.

9. Bocardo (OAO)

    Form:
    − Some $M$ are not $P$
    − All $M$ are $S$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\exists x \, (M(x) \land \lnot P(x))$
    − $\forall x \, (M(x) \rightarrow S(x))$
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    The first premise ensures at least one $M$ is outside $P$. Since all $M$ are also $S$, that $M$ is also an $S$. Thus, there exists an $S$ that is not $P$.

10. Camenes (AEE)

    Form:
    − All $P$ are $M$
    − No $S$ are $M$
    − $\therefore$ No $S$ are $P$

    Symbolization:
    − $\forall x \, (P(x) \rightarrow M(x))$
    − $\forall x \, (S(x) \rightarrow \lnot M(x))$
    − $\therefore$ $\forall x \, (S(x) \rightarrow \lnot P(x))$

    If being $P$ always means being $M$, but no $S$ can ever be $M$, then it follows that no $S$ can possibly be $P$.

11. Dimaris (IAI)

    Form:
    − Some $M$ are $P$
    − All $S$ are $M$
    − $\therefore$ Some $S$ are $P$
    Symbolization:
    − $\exists x \, (M(x) \land P(x))$
    − $\forall x \, (S(x) \rightarrow M(x))$
    − $\therefore$ $\exists x \, (S(x) \land P(x))$

    If at least one $M$ is a $P$, and all $S$ are $M$, then that $M$ is also an $S$, making some $S$ a $P$.

12. Felapton (EIO)

    Form:
    − No $M$ are $P$
    − All $M$ are $S$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\forall x \, (M(x) \rightarrow S(x))$
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    If nothing that is $M$ can be $P$, and all $M$ are also $S$, then some $S$ must fall outside $P$.

13. Ferison (EIO)

    Form:
    − No $M$ are $P$
    − Some $M$ are $S$
    − $\therefore$ Some $S$ are not $P$ 

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\exists x \, (M(x) \land S(x))$
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    If no $M$ is $P$, but some $M$ is also an $S$, then that $S$ cannot be a $P$.

14. Disamis (IAI)

    Form:
    − Some $M$ are $P$
    − All $M$ are $S$
    − $\therefore$ Some $S$ are $P$

    Symbolization:
    − $\exists x \, (M(x) \land P(x))$
    − $\forall x \, (M(x) \rightarrow S(x))$
    − $\therefore$ $\exists x \, (S(x) \land P(x))$

    If at least one $M$ is a $P$, and all $M$ are also $S$, then that same element is both $S$ and $P$.

15. Datisi (AII)

    Form:
    − All $M$ are $P$
    − Some $M$ are $S$
    − $\therefore$ Some $S$ are $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow P(x))$
    − $\exists x \, (M(x) \land S(x))$
    − $\therefore$ $\exists x \, (S(x) \land P(x))$

    If every $M$ is $P$, and at least one $M$ is also an $S$, then that individual is both $S$ and $P$.

16. Bramantip (AAI)

    Form:
    − All $P$ are $M$
    − All $M$ are $S$
    − $\therefore$ Some $S$ are $P$

    Symbolization:
    − $\forall x \, (P(x) \rightarrow M(x))$
    − $\forall x \, (M(x) \rightarrow S(x))$
    − $\therefore$ $\exists x \, (S(x) \land P(x))$

    If everything $P$ is $M$, and every $M$ is $S$, then the class of $P$ must overlap with $S$, so some $S$ are $P$.

17. Camenes (AEE)

    Form:
    − All $P$ are $M$
    − No $S$ are $M$
    − $\therefore$ No $S$ are $P$

    Symbolization:
    − $\forall x \, (P(x) \rightarrow M(x))$
    − $\forall x \, (S(x) \rightarrow \lnot M(x))$
    − $\therefore$ $\forall x \, (S(x) \rightarrow \lnot P(x))$

    If being $P$ always means being $M$, but no $S$ can ever be $M$, then it follows that no $S$ can possibly be $P$.

18. Fesapo (EAO)

    Form:
    − No $M$ are $P$
    − All $M$ are $S$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\forall x \, (M(x) \rightarrow S(x))$
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    If no $M$ can ever be $P$, and all $M$ are also $S$, then there must be some $S$ that are not $P$.

19. Fresison (EIO)

    Form:
    − No $M$ are $P$
    − Some $M$ are $S$
    − $\therefore$ Some $S$ are not $P$

    Symbolization:
    − $\forall x \, (M(x) \rightarrow \lnot P(x))$
    − $\exists x \, (M(x) \land S(x))$
    − $\therefore$ $\exists x \, (S(x) \land \lnot P(x))$

    If no $M$ is a $P$, but some $M$ are also $S$, then those $S$ cannot be $P$.
