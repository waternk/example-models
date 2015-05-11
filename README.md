## Example Models

This repository holds open source Stan models, data simulators, and real data.  There are models translating those found in books, most of the BUGS examples, and some basic examples used in the manual.

#### Books

* [Applied Regression Modeling](https://github.com/stan-dev/example-models/wiki/ARM-Models) (Gelman and Hill 2007)
* [Bayesian Cognitive Modeling](https://github.com/stan-dev/example-models/tree/master/Bayesian_Cognitive_Modeling) (Lee and Wagenmakers 2014)

#### BUGS examples

- [BUGS Models (volumes 1--3)](https://github.com/stan-dev/example-models/wiki/BUGS-Examples)

#### Basics

- Basic Distributions
- Basic Estimators

## Organization

Each example model should be organized to include the following

1.  Stan program(s) implementing the model (and variants),
2.  program to simulate data (in R or Python),
3.  simulated data file itself (for now in .data.R dump format)
4.  summary of output fit for simulated data file (text),
    a. check diagnostics (n_divergent is zero for all iterations, tree_depth < max_depth for all iterations, R_hat < 1.1)
    b. if diagnostics fail improve model with a note explaining the fix
5.  any real data sets with summary of fit (in original and Stan-readable format, with munging program from original to Stan-readable),
    a. check diagnostics (as above)
    b. if fit is poor then improve model with a note explaining the fix
6.  citations to source for model and/or data,
7.  documentation needed to understand the model (LaTeX, text, or HTML), including discussion of parameterizations and/or optimizations and their relations to performance (and to each other if there are multiple models),
8.  keywords or other tags to help organize by category (e.g., from manual, from BUGS volume, from book, involving logistic regression, application area such as population model, model type such as IRT or mark-recapture, etc.)
9.  author/copyright-holder info and open-source license info if not new BSD.

The idea is to encourage people to go through *all* of these steps for their models, particularly 3 and 4, which often get overlooked.

### Licensing

All of the example models are copyrighted by their author(s) or assignees under the new BSD license unless another open-source license is explicitly stipulated in the directory containing the model.
