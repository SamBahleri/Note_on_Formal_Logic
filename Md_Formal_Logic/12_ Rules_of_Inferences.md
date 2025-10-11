Rules of Inferences

Rules of inference are a list of rules used for natural deduction. Therefore, it is crucial to learn these rules before entering the natural deduction chapter.

## 1. Modus Ponens ($MP$)
The modus ponens rule is the process by which we affirm the antecedent.

First, we assume $$a \rightarrow b$$

Then, we consider it true that $$a$$

As a result, by logical consequence, then $$b$$

Overall, it can be written as follows:

$$\frac{a  \rightarrow b, \quad a}{\therefore b}$$

## 2. Modus Tollens ($MT$)
The modus tollens rule is the process by which we deny the consequent.

First, we assume $$a \rightarrow  b$$

Then, we consider it true that $b$ is not true, so $$\neg  b$$

As a result, by logical consequence, then $$\neg a$$

Overall, it can be written as follows:

$$\frac{a \rightarrow b, \quad \neg b}{\therefore \neg a}$$

## 3. Hypothetical Syllogism ($HS$)
Hypothetical Syllogism is a chain of proof, or often also called Transitive. The process is as follows:

First, we assume that $$a \rightarrow b$$

Then, we assume $$b \rightarrow c$$

So logically we can assume that $$a \rightarrow c$$ can be considered true

Overall, it can be written as follows:

$$\frac{a \rightarrow b, \quad b \rightarrow c}{\therefore a \rightarrow c}$$

## 4. Disjunctive Syllogism ($DS$)
The reasoning process of $DS$ is by eliminating one of the propositions. For example:

We assume $$a \lor b$$

Then from that statement, we know that $$\neg a$$

So, the final result is $$b$$

Overall, it can be written as follows:

$$\frac{a \lor b, \quad \neg a}{\therefore b}$$

## 5. Constructive Dilemma ($CD$)
Constructive Dilemma is a form of deductive reasoning that combines two conditional propositions with a disjunction. The pattern is as follows:

1. First premise:  
   $$a \rightarrow b$$

2. Second premise:  
   $$c \rightarrow d$$

3. Third premise (disjunction on the antecedent):  
   $$a \lor c$$

4. Then the conclusion is:  
   $$b \lor d$$

Overall, the general form of Constructive Dilemma can be written as follows:

$$
\frac{a \rightarrow b, \quad c \rightarrow d, \quad a \lor c}{\therefore b \lor d}
$$

## 6. Addition ($Add$)

The Addition ($Add$) pattern is one of the simplest forms of inference. Essentially, if we have a true proposition, then we can add another proposition through logical operations (disjunction or conjunction).

For example, suppose we know that:  
$$a$$

Then, we can add another proposition and obtain:

1. With disjunction:  
  $$a \lor b$$

    Overall, it can be written as follows:

    $$
    \frac{a}{\therefore a \lor b}
    $$

2. With conjunction:  
  $$a \land c$$

    Overall, it can be written as follows:

    $$
    \frac{a}{\therefore a \land c}
    $$

## 7. Simplification ($Simp$)

The Simplification ($Simp$) pattern, also called Conjunction Elimination, is an inference rule that allows us to draw conclusions from a conjunction. If we know that a conjunction is true, then each part of that conjunction is also true.

For example, suppose we have:  
$$a \land b$$

Then we can conclude:  
$$a$$  
or  
$$b$$

In general, the Simplification pattern can be written as follows:

$$
\frac{a \land b}{\therefore a}
\qquad \text{or} \qquad
\frac{a \land b}{\therefore b}
$$

## 8. Disjunction Elimination ($DE$)

The Disjunction Elimination pattern is an inference rule that allows us to draw conclusions from a disjunction. If we know that a disjunction is true, and from each of its alternatives we can conclude the same proposition, then we can conclude that proposition.

For example, suppose we have:  
$$a \lor b$$  
$$a \rightarrow c$$  
$$b \rightarrow c$$  

Then we can conclude:  
$$c$$  

In general, the Disjunction Elimination pattern can be written as follows:  

$$
\frac{a \lor b, \quad a \rightarrow c, \quad b \rightarrow c}{\therefore c}
$$  

## 9. Resolution ($Res$)

The Resolution ($Res$) pattern is an inference rule widely used in formal logic and automated proof. This rule works by eliminating a proposition and its negation from two disjunctions, to then produce a new disjunction.

In general, if we have:  
$$(a \lor b), \quad (\lnot a \lor c)$$  

Then we can conclude:  
$$b \lor c$$  

In other words, variable $a$ is eliminated because it appears in positive form in the first premise, and in negative form in the second premise.

The Resolution pattern can be written as follows:

$$
\frac{a \lor b, \quad \lnot a \lor c}{\therefore b \lor c}
$$

## 10. Double Negation ($DN$)

The Double Negation ($DN$) pattern states that the double negation of a proposition is equivalent to the proposition itself. This means that if we have a proposition preceded by two negation signs, then both can be removed without changing the truth value.

In general:  
$$a \equiv \lnot \lnot a$$

The truth of the statement above can be proven with a truth table:

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$\lnot a$</th>
      <th>$\lnot \lnot a$</th>
      <th style="border: 2px solid red;">$a \equiv \lnot \lnot a$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

The Double Negation inference rule can be written as follows:

$$
\frac{\lnot \lnot a}{\therefore a}
$$

## 11. Commutation ($Comm$)

The Commutation ($Comm$) pattern states that the order of propositions connected by logical operations of conjunction ($\land$) and disjunction ($\lor$) can be exchanged without changing the truth value.

In general:  

1. For conjunction:  
  $$a \land b \equiv b \land a$$

2. For disjunction:  
  $$a \lor b \equiv b \lor a$$

The Commutation inference rule can be written as follows:

$$
\frac{a \land b}{\therefore b \land a}
\qquad \text{or} \qquad
\frac{a \lor b}{\therefore b \lor a}
$$

## 12. Association ($Assoc$)

The Association ($Assoc$) pattern states that grouping of propositions connected by conjunction ($\land$) and disjunction ($\lor$) does not affect the truth value. In other words, parentheses can be moved without changing the logical meaning.

In general:

1. For conjunction:  
  $$(a \land (b \land c)) \equiv ((a \land b) \land c)$$

2. For disjunction:  
  $$(a \lor (b \lor c)) \equiv ((a \lor b) \lor c)$$

The Association inference rule can be written as follows:

$$
\frac{a \land (b \land c)}{\therefore (a \land b) \land c}
\qquad \text{or} \qquad
\frac{a \lor (b \lor c)}{\therefore (a \lor b) \lor c}
$$

## 13. Distribution ($Dist$)

The Distribution ($Dist$) pattern states that conjunction ($\land$) can be distributed over disjunction ($\lor$), and vice versa. This rule allows us to change the form of a logical proposition without changing its truth value.

In general:

1. Conjunction over disjunction:  
  $$a \land (b \lor c) \equiv (a \land b) \lor (a \land c)$$

2. Disjunction over conjunction:  
  $$a \lor (b \land c) \equiv (a \lor b) \land (a \lor c)$$

The Distribution inference rule can be written as follows:

$$
\frac{a \land (b \lor c)}{\therefore (a \land b) \lor (a \land c)}
\qquad \text{or} \qquad
\frac{a \lor (b \land c)}{\therefore (a \lor b) \land (a \lor c)}
$$

## 14. De Morgan's Laws ($DeM$)

De Morgan's Laws ($DeM$) pattern states the relationship between negation and conjunction ($\land$) and disjunction ($\lor$). This law shows how the negation of a conjunction or disjunction can be rewritten in equivalent form.

In general:

1. Negation of conjunction:  
  $$\lnot (a \land b) \equiv (\lnot a \lor \lnot b)$$

2. Negation of disjunction:  
  $$\lnot (a \lor b) \equiv (\lnot a \land \lnot b)$$

The truth of the statement above can be proven with truth tables: 

Truth table 1:
<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th>$\neg b$</th>
      <th>$a \land b$</th>
      <th style="border: 2px solid red;">$\neg (a \land b)$</th>
      <th style="border: 2px solid red;">$\neg a \lor \neg b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

Truth table 2:
<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th>$\neg b$</th>
      <th>$a \lor b$</th>
      <th style="border: 2px solid red;">$\neg (a \lor b)$</th>
      <th style="border: 2px solid red;">$\neg a \land \neg b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

De Morgan's Laws inference rule can be written as follows:

$$
\frac{\lnot (a \land b)}{\therefore \lnot a \lor \lnot b}
\qquad \text{or} \qquad
\frac{\lnot (a \lor b)}{\therefore \lnot a \land \lnot b}
$$

## 15. Implication ($Impl$)

The Implication ($Impl$) pattern states that an implication can be rewritten in disjunctive form.

In general:  
$$a \rightarrow b \equiv \lnot a \lor b$$

The truth of the statement above can be proven with a truth table: 
<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\neg a$</th>
      <th>$\neg b$</th>
      <th style="border: 2px solid red;">$\neg a \lor b$</th>
      <th style="border: 2px solid red;">$a \rightarrow b$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

The Implication inference rule can be written as follows:

$$
\frac{a \rightarrow b}{\therefore \lnot a \lor b}
$$

## 16. Exportation ($Exp$)
The Exportation ($Exp$) pattern states that a nested implication is equivalent to an implication from the conjunction of antecedents.

In general (equivalence):
$$(a \rightarrow (b \rightarrow c)) \equiv ((a \land b) \rightarrow c)$$

The truth of the statement above can be proven with a truth table: 

<table> <thead> <tr> <th>$a$</th> <th>$b$</th> <th>$c$</th> <th>$\neg a$</th> <th>$\neg b$</th> <th>$\neg c$</th> <th>$b \rightarrow c$</th> <th style="border: 2px solid red;">$a \rightarrow (b \rightarrow c)$</th> <th>$a \land b$</th> <th style="border: 2px solid red;">$(a \land b) \rightarrow c$</th> </tr> </thead> <tbody> <tr> <td>1</td><td>1</td><td>1</td> <td>0</td><td>0</td><td>0</td> <td>1</td> <td style="border: 2px solid red;">1</td> <td>1</td> <td style="border: 2px solid red;">1</td> </tr> <tr> <td>1</td><td>1</td><td>0</td> <td>0</td><td>0</td><td>1</td> <td>0</td> <td style="border: 2px solid red;">0</td> <td>1</td> <td style="border: 2px solid red;">0</td> </tr> <tr> <td>1</td><td>0</td><td>1</td> <td>0</td><td>1</td><td>0</td> <td>1</td> <td style="border: 2px solid red;">1</td> <td>0</td> <td style="border: 2px solid red;">1</td> </tr> <tr> <td>1</td><td>0</td><td>0</td> <td>0</td><td>1</td><td>1</td> <td>1</td> <td style="border: 2px solid red;">1</td> <td>0</td> <td style="border: 2px solid red;">1</td> </tr> <tr> <td>0</td><td>1</td><td>1</td> <td>1</td><td>0</td><td>0</td> <td>1</td> <td style="border: 2px solid red;">1</td> <td>0</td> <td style="border: 2px solid red;">1</td> </tr> <tr> <td>0</td><td>1</td><td>0</td> <td>1</td><td>0</td><td>1</td> <td>0</td> <td style="border: 2px solid red;">1</td> <td>0</td> <td style="border: 2px solid red;">1</td> </tr> <tr> <td>0</td><td>0</td><td>1</td> <td>1</td><td>1</td><td>0</td> <td>1</td> <td style="border: 2px solid red;">1</td> <td>0</td> <td style="border: 2px solid red;">1</td> </tr> <tr> <td>0</td><td>0</td><td>0</td> <td>1</td><td>1</td><td>1</td> <td>1</td> <td style="border: 2px solid red;">1</td> <td>0</td> <td style="border: 2px solid red;">1</td> </tr> </tbody> </table>

The Exportation inference rule can be written in both directions as follows:

$$
\frac{a \rightarrow (b \rightarrow c)}{\therefore (a \land b) \rightarrow c}
\qquad \text{and} \qquad
\frac{(a \land b) \rightarrow c}{\therefore a \rightarrow (b \rightarrow c)}
$$

## 17. Contrapositive ($Contra$)

The Contrapositive rule states that an implication is equivalent to its contrapositive. This means that if a proposition has the form:  

$$a \rightarrow b$$  

then it is logically equivalent to:  

$$\lnot b \rightarrow \lnot a$$  

The truth of the statement above can be proven with a truth table: 

<table>
  <thead>
    <tr>
      <th>$a$</th>
      <th>$b$</th>
      <th>$\lnot a$</th>
      <th>$\lnot b$</th>
      <th style="border: 2px solid red;">$a \rightarrow b$</th>
      <th style="border: 2px solid red;">$\lnot b \rightarrow \lnot a$</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td><td>1</td><td>0</td><td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>1</td><td>0</td><td>0</td><td>1</td>
      <td style="border: 2px solid red;">0</td>
      <td style="border: 2px solid red;">0</td>
    </tr>
    <tr>
      <td>0</td><td>1</td><td>1</td><td>0</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
    <tr>
      <td>0</td><td>0</td><td>1</td><td>1</td>
      <td style="border: 2px solid red;">1</td>
      <td style="border: 2px solid red;">1</td>
    </tr>
  </tbody>
</table>

The Contrapositive inference rule can be written as follows:

$$
(a \rightarrow b) \equiv (\lnot b \rightarrow \lnot a)
$$

## 18. Reductio Ad Absurdum ($RAA$)

Reductio Ad Absurdum ($RAA$), often called indirect proof, is an inference rule that states that if by assuming the negation of a proposition we arrive at a contradiction, then that proposition must be true. In other words, if the assumption $\neg a$ produces a contradiction (for example $a \land \neg a$), then we can conclude that $a$ is true.  

For example, suppose we assume:  
$$\neg a$$  

and from that assumption we can derive a contradiction:  
$$a \land \neg a$$  

Then we can conclude that:  
$$a$$  

In general, the Reductio Ad Absurdum pattern can be written as follows:  

$$
\frac{\neg a \;\; \vdash \;\; (a \land \neg a)}{\therefore a}
$$

## 19. Conditional Proof ($CP$)

Conditional Proof ($CP$) is an inference rule used to prove implications. Essentially, if by assuming premise $a$ we can derive conclusion $b$, then we can conclude that $a \rightarrow b$ is true.

For example, suppose we want to prove:  
$$a \rightarrow b$$  

From the following complex series of statements:

1. $a \rightarrow (c \land d)$  
2. $c \rightarrow e$  
3. $d \rightarrow f$  
4. $e \land f \rightarrow b$  

Steps using Conditional Proof:

| Step | Statement | Justification |
|------|-----------|---------------|
| 1. | $a$ | Assumption (for $CP$) |
| 2. | $c \land d$ | Modus Ponens: Step 1, Premise 1 ($a \rightarrow (c \land d)$) |
| 3. | $c$ | Simplification: Step 2 |
| 4. | $d$ | Simplification: Step 2 |
| 5. | $e$ | Modus Ponens: Step 3, Premise 2 ($c \rightarrow e$) |
| 6. | $f$ | Modus Ponens: Step 4, Premise 3 ($d \rightarrow f$) |
| 7. | $e \land f$ | Conjunction: Step 5, Step 6 |
| 8. | $b$ | Modus Ponens: Step 7, Premise 4 ($e \land f \rightarrow b$) |
| 9. | $a \rightarrow b$ | Conditional Proof: Steps 1-8 |

If from assumption $a$ we can derive $b$, then we can conclude $a \rightarrow b$.

In general, the Conditional Proof pattern can be written as follows:  

$$
\frac{a \;\; \vdash \;\; b}{\therefore a \rightarrow b}
$$