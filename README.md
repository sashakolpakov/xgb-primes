# Experiments on prime distribution inference 

This Jupyter notebook accompanies (https://arxiv.org/abs/2308.10817)

Prime prediction using XGBoost (prime_prediction_xgboost.ipynb): 

- numbers are represented as binary N-bit strings with leading zeros
- each string in the dataset is labeled 0 (composite) or 1 (prime)
- Bayesian hyperparameter optimization is used over a wide search space

Two values of N are used:

- N = 18 for a quick check: learning the first 23000 primes
- N = 24 for a longer time: learning the first 1077871 primes

In both cases the true positive rate is very low, as theoretically predicted in (https://arxiv.org/abs/2308.10817)

Rate of convergence in the Erdos-Kac law (Erdos-Kac_law_convergence.ipynb):

- compute the empirical distribution of the number of prime divisors for positive integers up to N=24 bits: no convergence to normal is visible on the QQ plot or by using normality tests (we would need N=240 or even larger to see it)

- comparing to CLT applied to the binomial distribution: quick convergence to the normal distribution is easily observed
