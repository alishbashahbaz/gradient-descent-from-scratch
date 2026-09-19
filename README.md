# Gradient Descent from Scratch
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/alishbashahbaz/gradient-descent-from-scratch/blob/main/gradient_descent_project.ipynb)

A numerical optimization project implementing gradient descent from scratch in Python and analysing its convergence behaviour.

## Project Objective

The objective of this project is to find the value of a trainable parameter, $\theta$, that minimises a squared-error loss function using gradient descent.

The project also compares analytical and numerical gradients and validates the custom optimization result against SciPy.

## Mathematical Model

The model used is:

\[
\hat{r} = \theta z
\]

with:

- $z = 4$
- $r = 18$

The squared-error loss function is:

\[
J(\theta) = (4\theta - 18)^2
\]

The optimal value is:

\[
\theta^* = 4.5
\]

## Analytical Gradient

The derivative of the loss function is:

\[
\frac{dJ}{d\theta} = 32\theta - 144
\]

At $\theta = 3$:

\[
\frac{dJ}{d\theta} = -48
\]

## What I Implemented

- Gradient descent from scratch in Python
- Parameter, loss and gradient tracking across iterations
- Convergence visualisation using Matplotlib
- Numerical gradient using the central-difference method
- Analytical vs numerical gradient comparison
- Learning-rate experiments
- Comparison with SciPy optimization

## Learning Rate Experiment

The following learning rates were tested:

- `0.005` — converged slowly
- `0.02` — fastest stable convergence among the tested values
- `0.05` — converged with overshooting and oscillation
- `0.07` — diverged

Both linear and logarithmic loss plots were used to compare convergence behaviour.

## Gradient Validation

At $\theta = 3$:

- Analytical gradient: `-48`
- Numerical gradient: approximately `-48.000000000101295`

The difference was approximately:

`1 × 10^-10`

This confirmed that the analytical gradient implementation closely matched the numerical approximation.

## SciPy Comparison

The custom gradient descent produced:

`theta ≈ 4.499945`

SciPy's `minimize_scalar` returned:

`theta = 4.5`

The absolute difference was approximately:

`5.48 × 10^-5`

This shows that the custom implementation closely approximated the optimal solution.

## Tools Used

- Python
- SciPy
- Matplotlib
- Jupyter Notebook

## How to Run

1. Download or clone this repository.
2. Open `gradient_descent_project.ipynb` in Jupyter Notebook, VS Code, or Google Colab.
3. Run the notebook cells from top to bottom.

## Skills Demonstrated

- Numerical optimization
- Gradient descent
- Numerical differentiation
- Gradient checking
- Convergence analysis
- Scientific computing
- Mathematical modelling
- Data visualisation
