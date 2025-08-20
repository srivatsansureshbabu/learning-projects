# Multi-Layered Perceptron (MLP)

A **Multi-Layered Perceptron** is an extension of the Single-Layer Perceptron (SLP) that can learn **more complex, non-linear patterns**. Unlike the SLP, which can only separate data with a straight line, an MLP can separate patterns like XOR that a single layer cannot handle.  

---

## Recommended Knowledge / Practice

- **Single-Layer Perceptrons (SLP)**  
- **Logistic Regression**  
- **Linear Regression**  
- **Basic calculus** (for understanding gradients)  
- **Forward and Backward Passes**  

---

## What This Project Does

This MLP has:

- **One hidden layer** with multiple neurons.  
- **Weights and biases for each neuron**, including the hidden and output layers.  
- **Sigmoid activation functions** to introduce non-linearity.  
- **Training loop** using **forward pass**, **loss computation**, and **backpropagation**.  

It learns the **XOR** logical operator:

- **Input data**: `[0,0], [0,1], [1,0], [1,1]`  
- **Expected outputs**: `[0,1,1,0]`  

The network adjusts its weights and biases over multiple epochs so that its predictions match the XOR outputs.

---

## Key Ideas

1. **Forward Pass**:  
   Each layer computes `output = sigmoid(weights * input + bias)` to pass to the next layer.  

2. **Activation Functions**:  
   Non-linear functions (like sigmoid) that allow the network to solve problems that are **not linearly separable**.  

3. **Backpropagation**:  
   A method to **update weights and biases** based on the **error** at the output.  
   - Computes **gradients** of the loss with respect to weights and biases.  
   - Propagates these errors backward through the network to adjust all parameters.  

4. **Training vs. Testing**:  
   - **Training**: Repeatedly adjust weights and biases to minimize error.  
   - **Testing**: Feed inputs forward with the learned weights to check predictions.  

---

## Key Difference from SLP

| Feature | SLP | MLP |
|---------|-----|-----|
| Layers | 1 | 2+ (hidden + output) |
| Can solve XOR? | ❌ | ✅ |
| Non-linearity | No | Yes (via activations) |
| Complexity | Simple | Higher, requires backpropagation |

## Things to Experiment With

- **Initial Weights** – MLPs depend heavily on the first initialized weights. Run the training program multiple times and observe that sometimes the training works perfectly, and sometimes it struggles.  
- **Number of Epochs** – Experiment with more or fewer epochs to see how it affects learning and convergence.  
- **Monitoring Predictions** – Print predictions after each pass through the dataset and observe how they evolve over time.  
- **Learning Rate** – Adjust the learning rate to see how it impacts training speed and stability.  
- **Number of Hidden Neurons** – Change the number of neurons in hidden layers to explore network capacity.

