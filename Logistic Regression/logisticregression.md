# Logistic Regression

This is one of the most popular algorithms in machine learning, and a natural step after the perceptron.  
The key difference is the **sigmoid function**, which squashes outputs into probabilities between 0 and 1.  

---

## Recommended Knowledge

- **Linear equations**:  
  `y = weights * features + bias` → this is the raw prediction before applying the sigmoid.  

- **Sigmoid function**:  
  `σ(z) = 1 / (1 + e^(-z))`  
  This ensures the output is always between 0 and 1.  

- **Binary classification**:  
  Logistic regression is designed for yes/no questions — spam vs. not spam, pass vs. fail, cat vs. not cat.  

- **Training loop**:  
  Adjust weights and bias using gradient descent to minimize classification errors.  

- **Testing loop**:  
  Use the trained weights/bias to predict new data and check accuracy.  

---

## What This Project Does

We train a logistic regression model to classify data points into two categories.  

- **Input data**: Feature vectors (numerical values).  
- **Expected outputs**: 0 or 1 (binary labels).  

The model learns by adjusting weights and bias so that the **sigmoid output** matches the true labels.  

---

## Key Idea

Logistic regression doesn’t just draw a line — it also measures **confidence**.  

- Step 1: Compute `z = weights * features + bias`  
- Step 2: Apply sigmoid → `σ(z)` gives a probability between 0 and 1  
- Step 3: Threshold at 0.5 → predict **1** if ≥ 0.5, otherwise **0**  

This makes it more flexible than a perceptron, since it doesn’t just say yes/no, but also *how sure it is*.  
