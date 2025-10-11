
<h1 style="text-align: center; font-size: 3rem;">Argument</h1>

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

In our daily lives, we undoubtedly use logic to analyze things, whether it's someone's statement or a natural phenomenon we observe. Then, in analyzing something, we naturally hope that our analysis is correct, or that we can identify something was wrong, avoid it, or correct it so that it becomes right. In this section, we will specifically learn about arguments: what an argument is, the components that make up an argument, and what makes an argument valid or invalid. Studying arguments is certainly beneficial, whether in the social, academic, or interpersonal realm.

## 1. Component

### 1.1. Statement

A statement or proposition is a declarative sentence that has a definite truth value; it can be either true or false.  A mathematical statement is one example of a statement.

Example 1:

$$
\begin{align*}
1 &.\ \displaystyle\bigl[2<4 \ \wedge \ 4<7 \ \to \ 2<7 \bigr]
& 6 &.\ \left[\frac{5}{6}\right]^7 = \neg \neg \left[\frac{5^7}{6^7}\right] \\[2mm]
2 &.\ s =2 \to s^3 \cdot s^5 = s^8
& 7 &.\ \left[6^{1/2}\right]\left[6^{3/2}\right] \lor \neg \neg 6^2 \\[2mm]
3 &.\ a = 3 \to \sqrt[a]{8^2} \equiv 8^{2/3}
& 8 &.\ \log(4 \cdot 5) \equiv \log 4 + \log 5 \\[2mm]
4 &.\ \left[4 \cdot 5\right]^6 \equiv 4^6 \cdot 5^6
& 9 &.\ m = 3, e = 2 \to (m+e)^2 \equiv m^2 + 2(me) + e^2 \\[2mm]
5 &.\ \left[4^{5/1}\right]^6 \lor 4^{30}
& 10 &.\ n = 5, a = 2 \to (n-a)^2 \equiv n^2 - 2(na) + a^2 \\[4mm]
\end{align*}
$$

All of the examples above are mathematical statements with truth values that can be verified.

Example 2:

1. $ \text{All prime numbers are odd}$  
2. $\sqrt{a+b}  = \sqrt{a} + \sqrt{b} $
3. ${}^{9}\!log\,81 > {}^{2}\!log\,64 - {}^{2}\!log\,16$


The second set of examples are false statements. However, since each can be evaluated to a definite conclusion, Example 2 is also a statement.

### 1.2. Non-Statement

Consequently, any expression that does not have a definite truth value is not considered a statement.

For example:

1. “What time is it?”

2. “Close the door.”

3. “Wow, that’s amazing!”

4. “Who is running?”

### 1.3. Open sentence  

We also need to understand that an argument can contain open sentences, statements whose truth value is not yet determined.  

For example:  

1. $ x \text{ is a prime number}$  

2. $ \forall x, y, z (x, y, z \in \mathbb{Z} \mid x +y = z)$

3. $ n^2 + 1$ is divisible by $3$

4. $ p > 10$


Until we specify what $p$, $x$, $z$, or $y$ refer to, the truth cannot be judged. Once the variable is assigned, the open sentence becomes a proposition (a definite true/false statement). This distinction is central in predicate logic. 

### 1.4. Conclusion

Intuitively, we all understand what a conclusion is. A conclusion is the result derived from a set of premises, or in this case, when premises present facts, the conclusion is what we can logically derive from those facts.

Example 1:  

$
\begin{aligned}
\text{Premise 1:} \ & \text{All humans are living beings} \\
\text{Premise 2:} \ & \text{Socrates is a human} \\
\text{Conclusion:} \ & \text{Therefore, Socrates is a living being}
\end{aligned}
$

As we can observe, a conclusion is a deduction drawn from the facts. And in this example, the conclusion is clearly correct.

Example 2:  

$
\begin{aligned}
\text{Premise 1:} \ & 2, 3 \in \mathbb{R} \\
\text{Premise 2:} \ & 2 < 3 \\
\text{Conclusion:} \ & \text{Hence, } 2 = 3
\end{aligned}
$


In this example, it is true that 2 and 3 are elements of the real numbers, and it is also true that 2 is less than 3. However, the conclusion drawn 2 = 3 is false because it does not logically follow from the premises.

### 1.5. Inference  

Inference is not the same as a conclusion. A conclusion is the specific claim that logically follows from the premises, whereas an inference refers to the entire reasoning process that connects the premises to the conclusion.  

For example:  

$
\begin{aligned}
\text{Premise 1:} \ & \text{All students must take the final exam} \\
\text{Premise 2:} \ & \text{Elica is a student} \\
\text{Conclusion:} \ & \text{Therefore, Elica must take the final exam}
\end{aligned}
$


Here, the conclusion is simply:  
$$\text{“Elica must take the final exam.”}$$

The inference is the reasoning as a whole:

$$\text{“Because all students must take the final exam, and Elica is a student, it follows that Elica must take the final exam.”}$$

## 2. Formal and Informal
When analyzing an argument, we can approach it from two perspectives:

### 2.1. Formal Logic

As we will continue to study in this course, formal logic is the discipline that focuses on the form of the argument itself, regardless of the content or meaning of the statements. For example:

Recall:

$
\begin{aligned}
\text{Premise 1:} \ & \text{All humans are living beings} \\
\text{Premise 2:} \ & \text{Socrates is a human}
\end{aligned}
$


Previously, we drew a conclusion by reading the content of these premises (statements in natural language). In formal logic, however, we represent these premises using symbols. For instance, we can represent the entire natural language statement with symbols like $p, q, r, s$ and so on.

For example:

− $p$: All humans are living beings

− $q$: Socrates is a human

From these two premises, we can combine them using the conjunction symbol ($ \land $), resulting in: $p \land q$ . If we translate this back into natural language, it becomes: "All humans are living beings and Socrates is a human."

### 2.2. Informal Logic

If formal logic focuses on the form of the premises, informal logic focuses on the content of those premises. We’ve already seen examples of this above.

Recall:

$
\begin{aligned}
\text{Premise 1:} \ & \text{All humans are living beings} \\
\text{Premise 2:} \ & \text{Socrates is a human} \\
\text{Conclusion:} \ & \text{Therefore, Socrates is a living being}
\end{aligned}
$

The focus of informal logic is:

1. Are the premises reasonable?

2. Are the terms used clear?

3. Who is Socrates?

### 2.3. Formal vs Informal

It is important to understand that formal and informal logic each have their own limitations. Specifically, formal logic allows us to draw conclusions systematically and with certainty, because the rules of inference have already been clearly defined. In this kind of reasoning, we do not focus on the content of the statements, we focus solely on the process of drawing conclusions.

For example:

$$ \text{If } A \text{ is true and } B \text{ is true, then } A \land B \text{ (A and B) is true.}$$

In this case, the conclusion is valid because the rule of conjunction says so. However, we do not know what $ A $  or $ B $ actually represent. We don’t evaluate whether $ A $ or $ B $ are reasonable or relevant in real-life contexts. On the other hand, informal logic is more contextual, as it reflects what is actually happening in the real world. However, it is more difficult to evaluate objectively and is more vulnerable to bias or logical fallacies. Simply put, informal logic represents a form of reasoning that we often encounter in everyday life.

For example:

$\text{“Climate change is real because almost every scientist agrees on it, and we can see unusual weather patterns happening more frequently.”}$

In this case, the reasoning isn’t framed in formal symbols like $𝐴$ and $𝐵$. Instead, it relies on contextual evidence (scientific consensus, observed weather) and appeals to what is happening in the real world. While it can be persuasive, it is also open to subjective interpretation, selective use of evidence, or possible fallacies (e.g., appeal to authority, hasty generalization).

## 3. Syllogism

As we have seen above, an argument is a collection of statements, and its conclusion, whether true or false, depends not only on the truth value of the statements, but also on whether the conclusion logically follows from the premises. Below are some examples of drawing conclusions from two premises and a conclusion, presented in both formal notation and natural language, which we understand as the process of syllogism.

1. Barbara (AAA)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } M \text{ are } P \\
    \text{Premise 2:} \ & \text{All } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, All } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All mammals are warm-blooded} \\
    \text{Premise 2:} \ & \text{All dogs are mammals} \\
    \text{Conclusion:} \ & \text{Therefore, All dogs are warm-blooded}
    \end{aligned}
    $

2. Celarent (EAE)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{All } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, No } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No reptiles are warm-blooded} \\
    \text{Premise 2:} \ & \text{All snakes are reptiles} \\
    \text{Conclusion:} \ & \text{Therefore, No snakes are warm-blooded}
    \end{aligned}
    $

3. Darii (AII)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } M \text{ are } P \\
    \text{Premise 2:} \ & \text{Some } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All books are sources of knowledge} \\
    \text{Premise 2:} \ & \text{Some objects are books} \\
    \text{Conclusion:} \ & \text{Therefore, Some objects are sources of knowledge}
    \end{aligned}
    $

4. Ferio (EIO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{Some } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No cats are reptiles} \\
    \text{Premise 2:} \ & \text{Some pets are cats} \\
    \text{Conclusion:} \ & \text{Therefore, Some pets are not reptiles}
    \end{aligned}
    $

5. Cesare (EAE)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } P \text{ are } M \\
    \text{Premise 2:} \ & \text{All } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, No } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No reptiles are mammals} \\
    \text{Premise 2:} \ & \text{All snakes are reptiles} \\
    \text{Conclusion:} \ & \text{Therefore, No snakes are mammals}
    \end{aligned}
    $
 
6. Camestres (AEE)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } P \text{ are } M \\
    \text{Premise 2:} \ & \text{No } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, No } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All birds are animals} \\
    \text{Premise 2:} \ & \text{No insects are animals} \\
    \text{Conclusion:} \ & \text{Therefore, No insects are birds}
    \end{aligned}
    $

7. Festino (EIO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{Some } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No fish are mammals} \\
    \text{Premise 2:} \ & \text{Some pets are fish} \\
    \text{Conclusion:} \ & \text{Therefore, Some pets are not mammals}
    \end{aligned}
    $

8. Baroco (AOO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } P \text{ are } M \\
    \text{Premise 2:} \ & \text{Some } S \text{ are not } M \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All animals are living beings} \\
    \text{Premise 2:} \ & \text{Some creatures are not animals} \\
    \text{Conclusion:} \ & \text{Therefore, Some creatures are not living beings}
    \end{aligned}
    $

9. Bocardo (OAO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{Some } M \text{ are not } P \\
    \text{Premise 2:} \ & \text{All } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{Some books are not fiction} \\
    \text{Premise 2:} \ & \text{All books are readable materials} \\
    \text{Conclusion:} \ & \text{Therefore, Some readable materials are not fiction}
    \end{aligned}
    $

10. Camenes (AEE)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } P \text{ are } M \\
    \text{Premise 2:} \ & \text{No } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, No } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All birds are animals} \\
    \text{Premise 2:} \ & \text{No reptiles are animals} \\
    \text{Conclusion:} \ & \text{Therefore, No reptiles are birds}
    \end{aligned}
    $


11. Dimaris (IAI)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{Some } M \text{ are } P \\
    \text{Premise 2:} \ & \text{All } S \text{ are } M \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{Some fruits are sweet} \\
    \text{Premise 2:} \ & \text{All apples are fruits} \\
    \text{Conclusion:} \ & \text{Therefore, Some apples are sweet}
    \end{aligned}
    $

12. Felapton (EIO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{All } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No dogs are reptiles} \\
    \text{Premise 2:} \ & \text{All dogs are animals} \\
    \text{Conclusion:} \ & \text{Therefore, Some animals are not reptiles}
    \end{aligned}
    $

13. Ferison (EIO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{Some } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No reptiles are mammals} \\
    \text{Premise 2:} \ & \text{Some reptiles are snakes} \\
    \text{Conclusion:} \ & \text{Therefore, Some snakes are not mammals}
    \end{aligned}
    $

14. Disamis (IAI)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{Some } M \text{ are } P \\
    \text{Premise 2:} \ & \text{All } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{Some fruits are sweet} \\
    \text{Premise 2:} \ & \text{All fruits are consumable items} \\
    \text{Conclusion:} \ & \text{Therefore, Some consumable items are sweet}
    \end{aligned}
    $

15. Datisi (AII)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } M \text{ are } P \\
    \text{Premise 2:} \ & \text{Some } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All books are sources of knowledge} \\
    \text{Premise 2:} \ & \text{Some books are novels} \\
    \text{Conclusion:} \ & \text{Therefore, Some novels are sources of knowledge}
    \end{aligned}
    $


16. Bramantip (AAI)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All } P \text{ are } M \\
    \text{Premise 2:} \ & \text{All } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{All birds are animals} \\
    \text{Premise 2:} \ & \text{All animals are living beings} \\
    \text{Conclusion:} \ & \text{Therefore, Some living beings are birds}
    \end{aligned}
    $

17. Fesapo (EAO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{All } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No cats are reptiles} \\
    \text{Premise 2:} \ & \text{All cats are pets} \\
    \text{Conclusion:} \ & \text{Therefore, Some pets are not reptiles}
    \end{aligned}
    $

18. Fresison (EIO)  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No } M \text{ are } P \\
    \text{Premise 2:} \ & \text{Some } M \text{ are } S \\
    \text{Conclusion:} \ & \text{Therefore, Some } S \text{ are not } P
    \end{aligned}
    $

    Example:  

    $
    \begin{aligned}
    \text{Premise 1:} \ & \text{No mammals are fish} \\
    \text{Premise 2:} \ & \text{Some mammals are pets} \\
    \text{Conclusion:} \ & \text{Therefore, Some pets are not fish}
    \end{aligned}
    $
