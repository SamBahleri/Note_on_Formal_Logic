<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;">
Well-Formed Formula
</h1>

</div>

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

A Well-formed formula, often abbreviated as Wff, is a method for constructing sentences that we refer to as syntax. The formation of a Wff is similar to grammar in natural languages, in that there are specific rules to ensure the language can be understood. While natural languages use alphabets, Wffs in Formal Logic use symbols.

## 1. Expression

A Well-formed formula (Wff) can be formed using the following symbols:

1. Atomic Sentences:

$$a, b, c, \ldots, p, q, r, \ldots,\psi_1, \ldots, \psi_n$$

2. Connectives:  
   $$\lnot, \land, \lor, \rightarrow, \leftrightarrow$$

3. Brackets:  
   $$( \ , \ )$$

Using the rules above, we can construct a syntax as follows:  
If A is a Wff and represents a proposition, then $\lnot A$ and $\lnot\lnot A$ are also considered Wffs.  
Furthermore, if A and B are Wffs, we can combine them using connectives, such as:

1. $a \land b$  
2. $a \lor b$  
3. $a \rightarrow b$  
4. $a \leftrightarrow b$

We can also combine two or more atomic sentences, such as $\lnot x \lor y \rightarrow z$.  
In contexts involving three atomic sentences, to avoid ambiguity, we must use brackets to make the meaning clear, for example: $(\lnot x \lor y) \rightarrow z$.

Below are some examples of compound forms of Wffs:

1. $\lnot a$
2. $a \lor b$
3. $(a \lor b) \rightarrow c$
4. $((a \land b) \lor (a \lor b)) \rightarrow c$
5. $(a \rightarrow b) \lor z$
6. $\lnot a \rightarrow b$
7. $\lnot x \rightarrow \lnot y$
8. $(a \rightarrow \lnot y) \land z$
9. $(((a \rightarrow \lnot y) \land \lnot\lnot z) \lor (a \lor b)) \rightarrow c$

Well-formed formulas (WFFs) not only serve as symbolic representations of propositions in formal logic, but also play an important role in avoiding the ambiguity that often arises in natural language. In everyday communication, meaning can often be unclear due to language structure or the multiple meanings of a word. The two main types of ambiguity in natural language are:

### 1.2. Lexical Ambiguity

This type of ambiguity occurs when a single word has more than one meaning.

Example 1:

Word:

$$\text{“Tail.”}$$

This word can mean:

1. An animal’s tail (the rear part of an animal’s body)
2. An airplane’s tail (the rear part of an aircraft)

If someone says over the phone: “I’m holding the tail,” the listener might ask: “Which tail? An animal’s tail or an airplane’s tail?”  
Without context or clarification, the meaning of the word “tail” becomes unclear (ambiguous).

Example 2:

Word:

$$\text{“Bank.”}$$

This word can mean:

1. A financial institution (where you store money)
2. The edge of a river (river bank)

Example 3:

Ambiguous sentence:

$$\text{“I’m sitting at the bank.”}$$

Possible interpretations:

1. Are you sitting at a river bank?
2. Or inside a banking institution?

### 1.3. Structural Ambiguity

Structural (syntactic) ambiguity happens when the structure or grammar of a sentence allows more than one interpretation, even if all words are clear individually.

Example 1:

$$\text{“I saw the man with the telescope.”}$$

Interpretation: “I used a telescope to see the man”  
or “I saw a man who was holding a telescope.”

Example 2:

$$\text{“He watched the dog with one eye.”}$$

Interpretation: “He used one eye to watch the dog”  
or “He watched a dog that had one eye.”

This is why formal logic is extremely useful for expressing sentences in a way that avoids ambiguity.

Example 3:

Without Parentheses:  
$$a \lor g \lor h$$

If we don’t use parentheses, the expression above can have two possible interpretations:

$$(a \lor g) \lor h \quad \text{or} \quad a \lor (g \lor h)$$

However, if we explicitly use parentheses, the meaning becomes clear, for example:

$$a \lor (g \lor h)$$

Let’s define the variables:

− $a$: “It is raining”  
− $g$: “I will take an umbrella”  
− $h$: “I will wear a raincoat”

Without parentheses, the expression $a \lor g \lor h$ is ambiguous.

In natural language, it might translate to something unclear like:

$$\text{“Either it rains, or I take an umbrella or coat.” (unclear grouping)}$$

With parentheses, as in $a \lor (g \lor h)$, the ambiguity is resolved.

This expression in natural language would be:

$$\text{“Either it is raining, or I will take an umbrella or a raincoat.”}$$

By grouping $g \lor h$ first, it’s clear that the umbrella and raincoat are alternative options, distinct from the possibility of rain.

The same principle applies to negation. Consider the difference between:

$$\lnot (a \lor b) \quad \text{and} \quad \lnot a \lor b$$

These have very different meanings:

1. $\lnot (a \lor b)$: “Not $a$ and not $b$” (i.e., neither $a$ nor $b$ is true)
2. $\lnot a \lor b$: “Either $a$ is false, or $b$ is true”

Using parentheses properly in formal logic ensures clarity and prevents misinterpretation.
