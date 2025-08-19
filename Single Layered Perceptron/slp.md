# Single Layer Perceptron (SLP)

This is one of the simplest projects in low-level machine learning, and a great place to start.

---

## Recommended Knowledge

- **Linear equations**:  
  `y = mx + b` → in machine learning we write it as  
  `y = weights * features + bias`

- **Weights** → Think of these as “importance multipliers.” The bigger the weight, the more that feature matters.  
- **Bias** → A shifting value that helps move the decision boundary up or down.  
- **Epoch** → One full pass over the training data. Like reviewing a practice test once — usually, you need multiple passes.  
- **Training loop** → The learning process, where weights and bias are adjusted based on errors.  
- **Testing loop** → The evaluation step, where we check if the model predicts correctly.

---

## What This Project Does

We train a perceptron (a single “neuron”) to learn the **AND** logical operator.  

- **Input data**: `[0,0], [0,1], [1,0], [1,1]`  
- **Expected outputs**: `[0,0,0,1]`  

The perceptron learns by repeatedly adjusting its weights and bias until its predictions match the AND function.

---

## Key Idea

The perceptron tries to **draw a line (or hyperplane)** that separates outputs into 0 or 1.  
If the sum of `inputs * weights + bias` is greater than 0, the perceptron predicts **1**, otherwise **0**.
