# Symbolization


Before we symbolizing statements using formal logical symbols, its important to clarify two key concepts. Firts, The object Language, and second, The Metalanguage:

1. Th Object Language

    The object Language is the formal language we analyze, consiting symbols like $p, q, \wedge, \vee, \neg$, and sentences we form with these symbols

2. The Metalanguage

    The Meta Language is the language we use to talk  about this object language, wich in this article is mostly English. We sue the Metalanguage to explain the meanning and rules of the Object Language, such as what makes  a formulawell-formed or how the connectives function.

When talking about Symbolization, we are dealing with the role of symbols, their purpose, and their essence as a formal system in analyzing and representing the truth of what is conveyed through symbols. However, once again, we must remember that in the previous material, we learned that the formal and informal, where the processes are deduction and induction, complement each other. Then, arguments formed from premises that are not logically connected can result in invalid forms, even though the content of those premises may be factually true. Furthermore, sound reasoning is reasoning based on the following points:

1. The initial stage of reasoning is empirical experience

2. The second stage is representation in natural language

3. The third stage is symbolic abstraction

### 1. Role

1) Proposition

    Remember that a proposition like “All humans are living beings” can be represented simply by $p$, and the same applies to other propositions, which can be symbolized as $p$, $q$, $r$, $s$, etc.

2) Relation

    To express logical relations between propositions in symbolic form, we first need to understand how these relations are conveyed through logical symbols. These symbols represent the connections between propositions and serve as the foundation for constructing arguments in propositional logic (PL). The key types of logical symbols used to represent these connections are called truth-functional connectives. These connectives determine the truth value of a compound proposition solely based on the truth values of its component propositions. Some commonly used truth-functional connectives include:

    1) Disjunction ($\lor$)

        In everyday language, the word “or” can represent two meanings: first, inclusive or, and second, exclusive or. At this initial stage, we will focus on learning inclusive or first. It is important to remember that the word “or” in formal logic is not the same as the word “or” used to indicate equivalence. For example:

        $$
        \text{Orang utan or Pongo pygmaeus}
        $$

        In this context, ‘or’ is used in a definitional or equivalence sense, which is different from the logical connective disjunction. Logical equivalence is expressed with the biconditional ($\leftrightarrow$)

        This kind of “or”:

        a. It does not represent a truth value (true or false), meaning there is no choice involved.

        b. It is definitional in nature.

        The representation of the relation expressed by logical "or" is as follows:

        Example 1:

        $$ \text {1+1 = 2 } \quad \text{or} \quad \text{3-2=1} $$

        Let:

        − $p$: $1 + 1 = 2$

        − $q$: $3 - 2 = 1$

        Then the symbolic form is:

        $$
        p \lor q
        $$

        Example 2:

        $$ \text {Koala } \quad \text{and} \quad \text{panda} $$

        Let:

        − $k$: Koala

        − $p$: Panda

        Then the symbolic form is:

        $$
        k \lor p
        $$

    2) Conjunction ($\land$)

        In everyday language, the word “and” is used to connect two propositions or statements, both of which are expected to be true or to occur simultaneously. In symbolic logic, this relation is represented by the symbol $\land$, known as conjunction.

        Example 1:

        $$ \text {1 < 2} \quad \text{and} \quad \text{3 > 2} $$

        Let:

        − $x$: $1 < 2$

        − $y$: $3 > 2$

        Then the symbolic form is:

        $$
        x \land y
        $$

        Example 2:

        $$ \text {Sun} \quad \text{and} \quad \text{Moon} $$

        Let:

        − $s$: Sun

        − $m$: Moon

        Then the symbolic form is:

        $$
        s \land m
      $$

    3) Conditional ($\rightarrow$)

        Conditional logic is a form of logic that represents the logical relationship between two events, the first is called the antecedent, and the second is the result or consequent.

        Example 1:

        $$\text {If it rains, then the ground will be wet.}$$

        Let:

        − $r$: It rains

        − $w$: The ground is wet

        Then, in symbolic form:

        $$
        r \rightarrow w
        $$

    4) Negation ($\neg$)

        Negation is a form of logic that represents the denial or rejection of a proposition, regardless of whether the proposition is true or false. In formal logic notation, negation is typically represented by the symbol ¬ or ~. Negation plays an important role in various forms of logical reasoning, one of which is Reductio ad absurdum (reduction to absurdity). In this method, we deliberately assume that the proposition we want to prove is false (i.e., it is negated), and then derive various logical consequences from that assumption. If the result leads to a contradiction or absurdity, then the initial assumption (the negation of the proposition) must be false, which means that the original proposition is true.

        Example:

        Let:

        − $p$: All prime numbers are odd

        We know that the statement above is false, so in symbolic form: 

        $$
        \neg p
        $$

        This means $ \text{not p}$, because the number 2 is a prime number and even, which contradicts the original statement. Therefore, we negate the statement.

    5) Biconditional ($\leftrightarrow $)

        Biconditional logic is a type of relational logic, similar to implication. However, the difference is that biconditional logic requires both propositions to have the same truth value, either both true or both false.

        Example 1:

        $$\text {Laika is a dog if and only if she is a mammal.}$$

        Let:

        − $l$: Laika is a dog

        − $m$: She is a mammal

        Then, in symbolic form:

        $$
        l \leftrightarrow m
        $$

        Example 2:

        $$\text {3 is a prime number if and only if it has exactly two positive divisors.}$$

        Given:

        − $p$ : 3 is a prime number

        −  $d$:  3 has exactly two positive divisors

        Then, in symbolic form:

        $$ p\leftrightarrow d$$

### 2. Purpose
The purpose of using logical symbols is to represent the truth value of a statement in a formal and systematic way. By using symbols, we can express and analyze the relationships between propositions accurately, consistently, and free from the ambiguities of natural language. To draw logical conclusions from a combination of several propositions ($p$, $q$, $r$, $s$), we must first know the truth value of each individual proposition. In propositional logic, each proposition has only two possible truth values:

1. True, represented by $T$ or the number $1$

2. False, represented by $F$ or the number $0$

Each proposition represents a single statement and has its own truth value, depending on the context or situation being discussed. To represent all possible truth values of one or more propositions, as well as the results of logical operations, we use a tool called a truth table. We will learn it in the next chapter
