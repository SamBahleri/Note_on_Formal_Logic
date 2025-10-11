
# Natural Deduction Rules 

After comprehending the rules of inference, we will have a better grasp of what natural deduction is. The most well-known idea of natural deduction is the work of [Frederic Fitch](https://en.wikipedia.org/wiki/Frederic_Fitch). He created a system known as the *Fitch-style calculus*. With this system, we can mechanically derive propositions to reach a valid conclusion, based on the initial premises or statements.

## 1. Conjunction

a. Conjunction Introduction

<div class="image-container">
    <img src="/Natural_Deduction/1_And_Intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 1:  Conjunction Introduction
    </div>
</div>

b. Conjunction Elimination

<div class="image-container">
    <img src="/Natural_Deduction/1_And_Elim.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 2:  Conjunction Elimination
    </div>
</div>

## 2. Disjunction

a. Disjunction Introduction

<div class="image-container">
    <img src="/Natural_Deduction/2_Or_Intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 3:  Disjunction Introduction
    </div>
</div>

b. Disjunction Elimination

<div class="image-container">
    <img src="/Natural_Deduction/2_Or_Elim.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 4:  Disjunction Elimination
    </div>
</div>

## 3. Negation

a.  Negation Introduction

<div class="image-container">
    <img src="/Natural_Deduction/3_Neg_intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 5:  Negation Introduction
    </div>
</div>

b.  Negation Elimination

<div class="image-container">
    <img src="/Natural_Deduction/3_Neg_Elim.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 6:  Negation Elimination
    </div>
</div>

## 4. Implication

a. Implication Introduction

<div class="image-container">
    <img src="/Natural_Deduction/4_Imp_Intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 7:  Implication Introduction
    </div>
</div>

b. Implication Elimination

<div class="image-container">
    <img src="/Natural_Deduction/4_Imp_Elim.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 8:  Implication Elimination
    </div>
</div>

## 5. Bottom

<div class="image-container">
    <img src="/Natural_Deduction/5_Bot.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 9:  Bottom
    </div>
</div>

## 5. Reiteration ($R$)

<div class="image-container">
    <img src="/Natural_Deduction/6_R.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 10:  Reiteration
    </div>
</div>

## 7. Reductio Ad Absurdum ($RAA$)

<div class="image-container">
    <img src="/Natural_Deduction/7_RAA.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 11:  RAA
    </div>
</div>

## 8. Biconditional

a. Biconditional Introduction

<div class="image-container">
    <img src="/Natural_Deduction/8_Bicon_Intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 12:  Biconditional Introduction
    </div>
</div>

b. Biconditional Elimination

<div class="image-container">
    <img src="/Natural_Deduction/8_Bicon_elim.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 13:  Biconditional Elimination
    </div>
</div>

## 9. Double Negation ($DN$)

a. Double Negation Introduction

<div class="image-container">
    <img src="/Natural_Deduction/9_DN_Intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 14  Biconditional Introduction
    </div>
</div>

b. Double Negation Elimination

<div class="image-container">
    <img src="/Natural_Deduction/9_DN_Elim.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 15:  Biconditional Elimination
    </div>
</div>

## 10. De Morgan’s Laws ($DM$)

$$\neg (A\land B) \equiv \neg A \lor \neg B$$

<div class="image-container">
    <img src="/Natural_Deduction/10_DM.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 16:  De Morgan’s Laws
    </div>
</div>

$$\neg (A\lor B) \equiv \neg A \land \neg B$$

<div class="image-container">
    <img src="/Natural_Deduction/10_DM2.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 17:  De Morgan’s Laws
    </div>
</div>

## 11. Material Conditional

$$ A \rightarrow B \equiv \neg A \lor B$$

<div class="image-container">
    <img src="/Natural_Deduction/11_Material.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 18:  Material Conditional
    </div>
</div>

$$ \neg A \lor B  \equiv A \rightarrow B$$

<div class="image-container">
    <img src="/Natural_Deduction/11_Material2.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 19:  Material Conditional
    </div>
</div>

## 13. Conditional Proof ($CP$)

<div class="image-container">
    <img src="/Natural_Deduction/13_Cp_Intro.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 22:  Conditional Proof
    </div>
</div>

## 12. Contrapositive

$$ A \rightarrow B \equiv \neg B \rightarrow \neg A$$

<div class="image-container">
<img src="/Natural_Deduction/12_Contra.png" alt="Diagram" class="responsive-image">
<div class="image-caption">
     Picture 20:  Contrapositive
    </div>
</div>

$$ \neg B \rightarrow \neg A \equiv  A \rightarrow B $$

<div class="image-container">
<img src="/Natural_Deduction/12_Contra2.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 21:  Contrapositive
</div>
