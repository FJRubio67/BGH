## Bayesian inference

In this post, we will present an application of the GH model using Bayesian inference. 
For simplicity, we will use weakly informative priors for all of the parameters. 
This is, Gamma priors with parameters $(0.001,0.001)$ for the shape and scale parameters of the PGW baseline hazard, and normal priors with large variance for the regression parameters.

To sample from the posterior distribution, we will employ the adaptive Metropolis within Gibbs sampler implemented in the R package `spBayes`.

# Application

We will analyse the `Leuk` data set available in the R package `spBayesSurv`. 
This data contains information about 1043 acute myeloid leukemia patients. 
We will consider the time dependent effect of the variable `age` (${\bf \tilde{x}}$), and the hazard level effects of `age`, `sex`, `wbc`, and `tpi` (${\bf x}$).

See: [Bayesian survival analysis using a General Hazard Structure](https://rpubs.com/FJRubio/BGH)
