# Causal Inference Notes

1. **Causal Inference Without Models**
  a. In the case of discrete outcomes, if we can access the outcome of a subject with and without treatment *A*, then we can access whether there was a causal effect. With notation, we can define what a causal effect on an individual means: Suppose that $Y^{a=1}$ is the outcome of survival for a subject if they did receive treatment $A$. Then $Y^{a=1} \neq Y^{a=0}$ indicates a causal effect. Individual causal effects cannot be observed because of missing data from one of the two $Y$ counterfactual outcomes. Our *assumption* with counterfactual outcomes is that they cannot interfere with one another. Otherwise, outcomes would not be well-defined and would need to be qualified with statements indicating "no interaction between units", for instance.
  b. Instead of individual causal effects, average treatment effects .
