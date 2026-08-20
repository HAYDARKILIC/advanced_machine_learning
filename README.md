# Advanced Machine Learning

This repository contains the Jupyter Notebooks for the Advanced Machine Learning
course. Each notebook is the hands-on Python companion to the lecture slides: the
formulas from the theory are derived step by step, implemented from scratch with
NumPy, and then tested in an experiment that checks whether the algorithm really
behaves the way the theory claims.

The notebooks are **self-contained**. The "toolkit" cell at the top of each one
holds every implementation used in that lecture, so no additional package needs to
be installed — NumPy, SciPy and Matplotlib are all you need.

---

## Contents

| # | Notebook | Derived and implemented |
|---|----------|-------------------------|
| 01 | [Statistical Learning Theory](01_statistical_learning_theory.ipynb) | Empirical risk, bias–variance decomposition, effective degrees of freedom, learning curves, nested cross-validation and model selection bias |
| 02 | [Regularisation and Sparsity](02_regularization_and_sparsity.ipynb) | Ridge shrinkage in the SVD basis, lasso subgradient/KKT conditions, coordinate descent vs ISTA vs FISTA, the elastic-net grouping effect |
| 03 | [Kernel Methods](03_kernel_methods.ipynb) | RKHS and the representer theorem, Mercer/PSD checks, the C-SVM dual solved by SMO, kernel ridge regression, kernel PCA |
| 04 | [Gaussian Processes](04_gaussian_processes.ipynb) | GP prior and posterior, log marginal likelihood with analytic gradients, the evidence as Occam's razor, ARD relevance, calibration of the error bars |
| 05 | [EM and Latent Variable Models](05_em_latent_variables.ipynb) | The ELBO and why EM is monotone, GMM E/M steps, local optima and initialisation, BIC/AIC model selection, mixtures as density models |
| 06 | [Gradient Boosting](06_gradient_boosting.ipynb) | Second-order (Newton) boosting, the split-gain and leaf-value formulas, shrinkage, subsampling, early stopping, bagging vs boosting |
| 07 | [Automatic Differentiation and Backpropagation](07_autodiff_and_backprop.ipynb) | Reverse-mode autodiff on a tape, gradient checking, SGD/momentum/RMSProp/Adam/AdamW, warm-up plus cosine learning-rate schedules |
| 08 | [Conformal Prediction](08_conformal_prediction.ipynb) | Split conformal prediction, the conformal quantile, adaptive intervals from normalised scores, prediction sets, marginal vs conditional validity |

Every notebook closes with a short "what to take away" section that leads into the
next one; read in order, they form a single argument about capacity, uncertainty
and optimisation.

## Usage

```bash
git clone https://github.com/HAYDARKILIC/advanced_machine_learning.git
cd advanced_machine_learning
pip install numpy scipy matplotlib jupyterlab
jupyter lab
```

The notebooks are stored with their outputs executed, so they can be read directly
on GitHub or reproduced from scratch with "Restart & Run All".

## A note on correctness

The implementations in the code cells — SMO, the GP marginal-likelihood gradients,
the autodiff engine, the second-order boosting trees and so on — have been checked
against independent references: the SMO solution reproduces the support vectors and
decision function of a reference SVM implementation, the GP and autodiff gradients
are verified against central finite differences, and the monotonicity of EM and the
coverage rate of conformal prediction are confirmed numerically.

## References

* Hastie, Tibshirani & Friedman, *The Elements of Statistical Learning*, 2nd ed., 2009.
* Bishop, *Pattern Recognition and Machine Learning*, 2006.
* Rasmussen & Williams, *Gaussian Processes for Machine Learning*, 2006.
* Platt, "Sequential Minimal Optimization", MSR-TR-98-14, 1998.
* Chen & Guestrin, "XGBoost: A Scalable Tree Boosting System", KDD 2016.
* Tipping & Bishop, "Probabilistic Principal Component Analysis", JRSS-B, 1999.
* Loshchilov & Hutter, "Decoupled Weight Decay Regularization", ICLR 2019.
* Angelopoulos & Bates, "A Gentle Introduction to Conformal Prediction", 2023.

## License

MIT
