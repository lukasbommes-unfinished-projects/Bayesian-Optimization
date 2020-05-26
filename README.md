# Neural Network Hyper Parameter Search with Bayesian Optimization for MNIST Classification

This example demonstrates the usage of Bayesian optimization (BO) as implemented in [scikit-optimize](https://scikit-optimize.github.io/stable/index.html) for tuning the hyper parameters of a neural network. As compared to grid search or random search less hyper parameter combinations need to be evaluated to determine the near-optimal parameter configuration.

In each iteration of BO the neural network is trained with a different set of hyper parameters and its validation accuracy is computed. A gaussian process is fitted to the validation accuracy over the space of hyper parameters. An acquistion function which is a function of the fitted gaussian process is sampled for the next suitable hyper parameter combination which is expected to increase validation accuracy.

For a great tutorial on Bayesian information read [this article](https://distill.pub/2020/bayesian-optimization/).