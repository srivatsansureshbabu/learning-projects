# Linear Regression

## Recommended Math Concepts
- **Slope-intercept form**: y = mx + b  
- **Gradient descent**: adjusting m and b step by step in the direction that reduces error

---

## Introduction
This is a simple **linear regression model**, essentially finding a line of best fit in the form:

\[
y = wx + b
\]

where:
- **w** = weight (slope, like m in y = mx + b)  
- **b** = bias (intercept)  

The goal of this project is to learn how to use gradient descent to find the optimal `w` and `b` that minimize error between predicted values and true values.

---

## Example Problem
We want to map the values:

X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
Y = [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]


This is essentially doubling each input, so the true line is:

\[
y = 2x + 0
\]

Our model starts with **random weight and bias**, and uses **gradient descent** to converge toward this solution.

---

## Loss Function
We measure error using **Mean Squared Error (MSE)** for each point:

\[
\text{Error} = (y_{pred} - y)^2
\]

---

## Gradient Descent
To minimize error, we compute the gradients:

\[
\frac{\partial \text{Error}}{\partial w} = 2 \cdot (y_{pred} - y) \cdot x
\]

\[
\frac{\partial \text{Error}}{\partial b} = 2 \cdot (y_{pred} - y)
\]

These tell us how much to adjust `w` and `b` each step.

---

## Update Rules
\[
w := w - \text{learning rate} \cdot \frac{\partial \text{Error}}{\partial w}
\]

\[
b := b - \text{learning rate} \cdot \frac{\partial \text{Error}}{\partial b}
\]

---

## Visualization
During training, we collect snapshots of `(w, b)` and animate the line as it **moves closer to the best fit**. This makes gradient descent easier to understand.

---

## Key Takeaways
- Linear regression fits a straight line to data.  
- Gradient descent iteratively improves the line by reducing error.  
- Over time, `w → 2` and `b → 0` for this dataset.  
