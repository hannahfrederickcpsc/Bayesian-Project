# DS 6014: Bayesian Machine Learning Final Project

## Viewing Our Project

All code related to this project can be found in `Bayesian-Final-Code.ipynb` 

## Project Description

Our central question is as follows: can we use approaches such as Bayesian optimisation to automate the learning of tuning parameters for Hamiltonian Monte Carlo (HMC)? This was inspired by project proposals for a graduate-level Bayesian Machine Learning course at Cornell. From initial research, the parameters for HMC we will be tuning are: the step-size (𝜖) and the number of leapfrog steps taken (L). We are interested in seeing if we could use some optimization techniques related to this course material to try to more efficiently tune some of these parameters.

In order to adapt the MCMC parameters L and 𝜖 for HMC, we need to first use an objective function and then choose a suitable optimization method. The objective function that we will estimate is the expected squared jumping distance (ESJD) divided by the square root of L. This function normalizes the ESJD, which takes efficiency and computation into consideration. Then we will search over a grid of  L and 𝜖 values, seeking to use a Gaussian process to maximize the objective function estimate. This allows us to define an acquisition function, which informs our next choice of parameters. We are less interested in finding the absolute best values of hyperparameters, and instead will be focused on choosing sufficiently good hyperparameters; stressing an exploitation of known good hyperparameters over an exploration of new ones.

## References
Ziyu Wang, Shakir Mohamed, and Nando De Freitas. “Adaptive Hamil-tonian and Riemann Manifold Monte Carlo Samplers”. In:*Proceedings ofthe 30th International Conference on International Conference on Machine Learning - Volume 28*. ICML’13. Atlanta, GA, USA: JMLR.org,2013, III–1462–III–1470

Pasarica, Cristian and Gelman, Andrew. Adaptively scaling the Metropolis algorithm using expected squared jumped distance. Statistica Sinica, 20(1):343, 2010.

https://arxiv.org/pdf/1302.6182.pdf

## Authors
Hannah Frederick (hbf3k)   
Sean Grace (smg2mx)  
Annie Williams (maw3as)  
André Zazzera (alz9cb)


