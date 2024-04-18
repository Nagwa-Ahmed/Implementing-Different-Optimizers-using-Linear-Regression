# 📈 Implementing Different Optimizers for Linear Regression

The project aims to implement five first order optimizers and one second order optimizer from scratch using linear regression using python and applying OOP concepts

## 🚀 Overview

Gradient descent (GD) serves as the cornerstone optimizer in machine and deep learning, but it struggles with flat surfaces of loss functions. To address this, various variants of GD have been developed. One such variant is momentum GD, which addresses the issue of oscillations around minima by introducing momentum. Additionally, Nesterov Accelerated GD incorporates a lookahead step to further improve convergence.

While these GD variants maintain a fixed learning rate, Adagrad adjusts the learning rate based on feature sparsity, preventing the learning rate from becoming too small for dense features. RMSprop was introduced to address this issue by using an exponential weighted average of previous gradients.

In contrast to GD variants, which approximate the cost function linearly to reach the minimum, second-order optimizers like Newton-Raphson utilize the Hessian matrix. BFGS is an approximation of Newton-Raphson, providing faster convergence with convex loss functions.

## 📚 Libraries Used

- pandas
- numpy
- abc
- seaborn

## 🛠️ Implementation

The project utilizes a parent class, `Gradient_Descent`, from which all GD variants inherit. This parent class includes all iteration steps and an abstract method that is updated in each child class. Additionally, another abstract method is used for plotting iterations versus loss.

The following optimizers are implemented:

1. **Vanilla Gradient Descent:** Basic GD implementation.
2. **Momentum Gradient Descent:** Incorporates momentum to reduce oscillations.
3. **Nesterov Accelerated Gradient Descent (NAG):** Utilizes a lookahead step.
4. **Adagrad:** Adjusts the learning rate based on feature sparsity.
5. **RMSprop:** Addresses Adagrad's issue using an exponential weighted average of previous gradients.
6. **Quasi-Newton-Raphson:** Approximates Newton-Raphson using BFGS.

## 🚀 Usage

Each optimizer can be instantiated and applied to linear regression to estimate its coefficients.
