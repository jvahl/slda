# slda
This repository contains [Cython](http://cython.org/) implementations of [Gibbs
sampling](https://en.wikipedia.org/wiki/Gibbs_sampling) for [latent Dirichlet
allocation](https://en.wikipedia.org/wiki/Latent_Dirichlet_allocation) and
various supervised LDAs:

- supervised LDA (linear regression)
- binary logistic supervised LDA (logistic regression)
- binary logistic hierarchical supervised LDA (trees)
- generalized relational topic models (graphs)

[![Build Status](https://travis-ci.org/Savvysherpa/slda.png)](https://travis-ci.org/Savvysherpa/slda)

## Installation

This package only works with Python <=3.6.x. Conda users with newer Python versions can create and activate a Python 3.6 environment via

```bash
$ conda create -n py36 python=3.6 -y
$ conda activate py36
```

### Dependencies

#### GNU Scientific Library
This module depends on [GSL](http://www.gnu.org/software/gsl/), please install
it. For ubuntu users this is as simple as
```bash
$ sudo apt-get install libgsl-dev -y
```

### Instructions


#### pip install slda

If you want slda installed in your environment, run:
```bash
$ pip install git+https://github.com/jvahl/slda.git
```

## fix temporary issue with pypolyagamma and scipy

This package depends on pypolyagamma, which in turn depends on an older version of scipy. To downgrade scipy, run
```bash
$ pip install --upgrade scipy==1.2.1
```

## Tests

To run the tests, run
```bash
$ py.test slda
```
This may take as long as 15 minutes, so be patient.

## License

This code is open source under the MIT license.

This repository is forked from https://github.com/Savvysherpa/slda. The goal of this fork is to fix installation issues and make the package accessible to the broader public again.
