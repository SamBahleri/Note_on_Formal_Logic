<h1 style="text-align: center; font-size: 3rem; margin-top: 3rem; margin-bottom: 2rem;">  Semantic Tableaux </h1>

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

Semantic Tableaux, commonly called a truth tree, is an effective method for demonstrating the validity of a formula. The Semantic Tableaux method was developed by [Evert Willem Beth](https://en.wikipedia.org/wiki/Evert_Willem_Beth), a Dutch logician, in the 1950s. The process is similar to Fitch-style natural deduction, but Semantic Tableaux uses branches (arrows) on each proposition to indicate contradictions.

## 1. Conjunction Decomposition

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/1.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 1: Conjunction Decomposition
    </div>
</div>

## 2. Negated Conjunction Decomposition
<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/2.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 2: Negated Conjunction Decomposition
    </div>
</div>

## 3. Disjunction Decomposition
<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/3.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 3: Disjunction Decomposition
    </div>
</div>

## 4. Negated Disjunction Decomposition
<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/4.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 4: Negated Disjunction Decomposition
    </div>
</div>

## 5. Double Negation
<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/5.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 5: Double Negation
    </div>
</div>

## 6. Conditional Decomposition
<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/6.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 6: Conditional Decomposition
    </div>
</div>

## 7. Negated Conditional Decomposition

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/7.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 7: Negated Conditional Decomposition
    </div>
</div>

## 8. Biconditional Decomposition

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/8.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 8: Biconditional Decomposition
    </div>
</div>

## 9. Negated Biconditional Decomposition

<div class="image-container">
    <img src="/2_Logic_Blog/Branch_of_Logic/Formal_Logic/Trees/9.png" alt="Diagram" class="responsive-image">
    <div class="image-caption">
        Picture 9: Negated Biconditional Decomposition
    </div>
</div>
