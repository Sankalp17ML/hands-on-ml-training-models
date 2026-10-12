# Hands-On ML — Chapter 4: Training Models

A hands-on learning repository for Chapter 4 of *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow (3rd Edition)*.

## Goals
- Understand the mathematics behind training ML models.
- Implement algorithms using NumPy and Scikit-Learn.
- Visualize training behavior and evaluate models.
- Record experiments, observations, and learning notes.

## Topics
- Linear Regression - Done
- Gradient Descent
- Polynomial Regression
- Learning Curves
- Ridge, Lasso, and Elastic Net
- Logistic Regression
- Softmax Regression

## Repository Structure
- `notebooks/` — Chapter implementations and experiments
- `src/` — Reusable Python modules
- `data/` — Local datasets (excluded from Git)
- `notes/` — Concepts, equations, and observations

## Progress
- [ D ] Linear Regression
- [ ] Gradient Descent
- [ ] Polynomial Regression
- [ ] Regularized Linear Models
- [ ] Logistic Regression
- [ ] Softmax Regression

## Tech Stack
Python | NumPy | Pandas | Matplotlib | Scikit-Learn | Jupyter

## Reference
Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow — Aurélien Géron, 3rd Edition.


## Learning Progress

### Day 1 — Linear Regression

**Topics Covered:**
- Linear Regression and vectorized predictions
- Mean Squared Error (MSE) cost function
- Normal Equation and mathematical derivation
- Matrix transpose, inverse, and pseudoinverse
- Introduction to Singular Value Decomposition (SVD)
- Linear Regression using Scikit-Learn
- Introduction to Gradient Descent and Lipschitz continuity

**Implementations:**
- Generated a synthetic linear dataset using NumPy
- Calculated model parameters using the Normal Equation
- Made predictions using matrix multiplication
- Trained a model using Scikit-Learn's LinearRegression
- Compared manual and Scikit-Learn predictions

**Key Learning:**
Linear Regression finds model parameters that minimize
the Mean Squared Error. The Normal Equation provides
a direct mathematical solution, while the pseudoinverse
handles singular matrices.