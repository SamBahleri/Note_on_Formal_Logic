<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;">Identity and Quantity</h1>
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

## 1. Identity

Simply put, in logic, something is considered identical if $a$ is the same as $b$, symbolically written as $a = b$. However, we must be careful in understanding these two constants. Specifically, the term “identical“ here does not refer to two objects that are very similar, but rather to one and the same object. Empirically, because two different objects can never be truly identical. Identity does not speak of similarity, but of sameness, that $a$ and $b$ are not merely alike, but actually refer to the exact same entity. Consider the classic example from the philosophy of language, “Morning Star” and “Evening Star”, these are both names that refer to the same object, Venus. Another example, consider this expression, $\frac{1}{2} = 0.5$, logically we agree that this expression is same.

For example, Consider the “Morning Star” and “Evening Star”, we can symbolize these statements like this:

Let:

− $m$ = the Morning Star

− $e$ = the Evening Star

Then the identity claim is:

$$ m = e $$

This states that both names refer to one and the same object.

If we treat them as predicates:

− $MS(x)$ = “$x$ is the Morning Star”

− $ES(x)$ = “$x$ is the Evening Star”

Then we can express:

$$\exists x \, (MS(x) \land ES(x))$$

Meaning: *there exists an object $x$ such that $x$ is both the Morning Star and the Evening Star*.

Moreover, identity is not just a symbol but follows specific rules that govern how it works.

For example:

1. Reflexivity

    Every object is identical to itself. This is written as

    $$\forall x (x = x)$$

    which expresses the obvious fact that no matter what object we choose, it is always equal to itself.

    For example, let $P(x)$ mean “$x$ is a prime number.” If $x = 7$, then it must also be true that $7 = 7$. In predicate form, we can write this as

    $$\forall x \, (x = 7 \to x = x)$$

    And if we combine reflexivity with a property, we get

    $$\forall x \, (x = 7 \to (P(x) \leftrightarrow P(7)))$$

    This means that if $x = 7$, then whatever property $P$ applies to $x$ must also apply to $7$. For instance, if $P(x)$ means “$x$ is prime,” then since $x = 7$, $P(x)$ holds if and only if $P(7)$ holds.

2. Leibniz’s Law
    Leibniz’s Law, also called the principle of substitutivity of identicals. This states that if $x = y$, then whatever is true of $x$ is also true of $y$, symbolized as $$x = y \rightarrow (P(x) \leftrightarrow P(y))$$ If two names refer to the same object, then they are interchangeable in any true statement. For example, if $m = e$ (Morning Star = Evening Star), and the statement “$m$ is visible at dawn” is true, then it must also be true that “$e$ is visible at dawn.”

## 2. Quantity

In everyday language, we often encounter vagueness, even ambiguity, when interpreting someone’s statements. For example, consider the sentence: *“All humans love some dogs.”* The word *some* here is vague, because it is unclear how many dogs are being referred to, or whether all humans love the same dogs or different ones. This ambiguity can lead to different interpretations. For instance, the sentence can be understood in two distinct ways:

All humans love at least one dog. In predicate logic, this is written as

$$
\forall x \, (Human(x) \rightarrow \exists y \, (Dog(y) \land Loves(x,y)))
$$

This means: every human loves at least one dog, though the specific dog may differ from person to person.

There is some dog that all humans love. In predicate logic, this is written as

$$
\exists y \, (Dog(y) \land \forall x \, (Human(x) \rightarrow Loves(x,y)))
$$

This means: there exists a particular dog that is loved by all humans.

To avoid ambiguity, we can express the specific quantity of objects we are talking about. Predicate logic allows us to distinguish between *at least*, *at most*, and *exactly* a certain number of objects satisfying a condition $A(x)$.


1. At least (minimum number).
    This means there are at least $n$ different objects that satisfy $A(x)$, possibly more.

    a) At least one:

    $$
    \exists x \, A(x)
    $$

    This means: *“There exists at least one $x$ such that $A(x)$ is true.”*

    For example:

    Let $A(x)$ = “$x$ is a prime number.”
    Then the statement says: *“There is at least one prime number.”*
    This is true, since $x = 2$ works.

    b) At least two:

    $$
    \exists x \exists y \, (A(x) \land A(y) \land x \neq y)
    $$

    This means: *“There exist at least two different objects such that $A(x)$ holds.”*

    For example:
  
    Let $A(x)$ = “$x$ is a prime number.”
    Then the statement says: *“There are at least two prime numbers.”*
    This is true, because $x = 2$ and $y = 3$ both satisfy $A(x)$, and $2 \neq 3$.

    c) At least three:

    $$
    \exists x \exists y \exists z \, (A(x) \land A(y) \land A(z) \land x \neq y \land x \neq z \land y \neq z)
    $$

    This means: *“There exist at least three different objects such that $A(x)$ holds.”*

    For example:
    Let $A(x)$ = “$x$ is a prime number.”
    Then the statement says: *“There are at least three prime numbers.”*
    This is true, because $x = 2$, $y = 3$, and $z = 5$ all satisfy $A(x)$, and they are pairwise distinct.

2. At most (maximum number).
    This means there are no more than $n$ different objects satisfying $A(x)$.

    a) At most one:

    $$
    \forall x \forall y \, ((A(x) \land A(y)) \rightarrow x = y)
    $$

    This means: *“If $x$ and $y$ both satisfy $A$, then they must be the same object.”*

    For example:

    Let $A(x)$ = “$x$ is the even prime number.”
    Then the statement says: *“There is at most one even prime.”*
    This is true, since $2$ is the only even prime, and no two distinct numbers can both satisfy $A(x)$.

    b) At most two:

    $$
    \forall x \forall y \forall z \, ((A(x) \land A(y) \land A(z)) \rightarrow (x = y \lor x = z \lor y = z))
    $$

    This means: *“If $x$, $y$, and $z$ all satisfy $A$, then at least two of them are the same.”*
    So there cannot be three distinct objects satisfying $A(x)$.

    For example:

    Let $A(x)$ = “$x$ is a square root of $4$.”
    Then the statement says: *“There are at most two square roots of $4$.”*
    This is true, because the only solutions are $x = 2$ and $x = -2$.

    c) At most three:

    $$
    \forall x \forall y \forall z \forall w \, ((A(x) \land A(y) \land A(z) \land A(w)) \rightarrow (x = y \lor x = z \lor x = w \lor y = z \lor y = w \lor z = w))
    $$

    This means: *“If $x$, $y$, $z$, and $w$ all satisfy $A$, then at least two of them must be the same.”*  
    So there cannot be four distinct objects satisfying $A(x)$.

    For example:

    Let $A(x)$ = “$x$ is a primary color of light.”
    Then the statement says: *“There are at most three primary colors of light.”*
    This is true, since the only options are red, green, and blue.

3. Exactly (precise count).
    This means there are exactly $n$ distinct objects satisfying $A(x)$, not more, not less.

    a) Exactly one:

    $$
    \exists x \, (A(x) \land \forall y (A(y) \rightarrow y = x))
    $$

    This means: *“There exists exactly one object such that $A(x)$ holds.”*

    For example:

    Let $A(x)$ = “$x$ is the even prime number.”
    Then the statement says: *“There is exactly one even prime number.”*
    This is true, since $2$ is the only even prime.

    b) Exactly two:

    $$
    \exists x \exists y \, (A(x) \land A(y) \land x \neq y \land \forall z (A(z) \rightarrow (z = x \lor z = y)))
    $$

    This means: *“There exist exactly two distinct objects such that $A(x)$ holds.”*

    For example:

    Let $A(x)$ = “$x$ is a square root of $4$.”
    Then the statement says: *“There are exactly two square roots of $4$.”*
    This is true, since the solutions are $2$ and $-2$, and no others.

    c) Exactly three:

    $$
    \exists x \exists y \exists z \, (A(x) \land A(y) \land A(z) \land x \neq y \land y \neq z \land x \neq z \land \forall w (A(w) \rightarrow (w = x \lor w = y \lor w = z)))
    $$

    This means: *“There exist exactly three distinct objects such that $A(x)$ holds.”*

    For example:

    Let $A(x)$ = “$x$ is a primary color of light.”
    Then the statement says: *“There are exactly three primary colors of light.”*
    This is true, since the primary colors are red, green, and blue, no more, no less.
