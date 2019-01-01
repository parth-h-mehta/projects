# Projects
Bayesian ML models and probabilistic inference


### 1. A Dirichlet-Categorical Die
**Problem:** Prof. Persi Diaconis loves fair, icosahedron dice: [Link](https://www.jstor.org/stable/2324089). After numerous throws and prolonged usage, however, a die is seldom fair. Given 10,000 throw outcomes of an old, initially fair 20 sided die, can we confidently predict the probability that a certain die face will show up?
<br />**Theory**: Each die roll is merely a draw from the Categorical distribution. The Categorical distribution is a member of the Exponential family of distributions, so it is endowed, to our delight, with a conjugate prior: the Dirichlet distribution. Furthermore, the prior-likelihood conjugacy allows for the posterior (again latent Dirichlet like our prior) to be approximated well during stochastic variational inference. A significant benefit of using SVI is the ability to randomly sample subsets of data during ELBO estimates! We can thus tackle even large datasets with remarkable efficiency. While tempting, the use of objective hyper-parameters such as Jeffrey's prior is, arguably, inefficient: the die was originally fair, so it helps to put more weight on the hyper-parameters. Lastly, one side-effect of being (entirely) Bayesian is that we can indeed quantify our 'confidence': we can obtain the entire posterior distribution, instead of a single, point estimate like the MAP.
<br />**Code**: [Link](https://github.com/parth-h-mehta/projects/blob/local_branch/A%20Dirichlet-Categorical%20Die.ipynb)
