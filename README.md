# CYTools.jl

## Goal

The package CYTools.jl aims towards making the *entire* functionality of the Python package [CYTools](https://cytools.liammcallistergroup.com/about/) available in [Julia](https://julialang.org/). We base this project on [OSCAR](https://oscar.computeralgebra.de/) for general functionality on toric spaces, polyhedral geometry etc. Specialized algorithms (for CICYs, 3 and 4-dimensional reflexive polytopes in the Kreuzer-Skarke list) will be collected in this `Julia` package.

As long as infrastructure/architecture is concerned, the goal is to write code which would eventually allow for a full-scale integration into [OSCAR](https://oscar.computeralgebra.de/). Such an integration would have to be discussed in more detail once the time comes.

On the long run, a key step towards writing this package is to re-write core algorithm of the existing [CYTools](https://cytools.liammcallistergroup.com/about/) in a small and self-contained C++ project. Upon wrapping this code, this functionality can then be made available in `Julia` (but also in other languages, such as [Python](https://www.python.org/) or other large software projects ([Macaulay2](http://www2.macaulay2.com/Macaulay2/), [Sage](https://www.sagemath.org/),...) or even commercial software such as [Mathematica](https://www.wolfram.com/mathematica/)). This approach has the added advantage that large libraries (e.g. [CGAL](https://www.cgal.org/)) need not be included. So on the long run, this package should be slim and easily to install.


## Status

This project just began. We are currently in the process of initiating the code migration from [CYTools](https://cytools.liammcallistergroup.com/about/). This we hope to yield a first functional `Julia` version by fall 2022. Further code optimization (in particular increased performance) is saved for a later stage of this project.


## Code coverage and tests

* [![CI](https://github.com/HereAround/CYTools.jl/actions/workflows/CI.yml/badge.svg?branch=master)](https://github.com/HereAround/CYTools.jl/actions/workflows/CI.yml)
* [![pages-build-deployment](https://github.com/HereAround/CYTools.jl/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/HereAround/CYTools.jl/actions/workflows/pages/pages-build-deployment)
* [![codecov](https://codecov.io/gh/HereAround/CYTools.jl/branch/master/graph/badge.svg?token=RX0SNJAVQZ)](https://codecov.io/gh/HereAround/CYTools.jl)


## Installation instructions for Linux

1. Install `Julia` on your computer. The latest version can be found [here](https://julialang.org/downloads/).
2. Download this development version of `CYTools.jl`. Those interested in contributing should instead clone this repository: 
```
    git clone https://github.com/HereAround/CYTools.jl.git
```
3. Place your clone/download in a location outside of the `.julia` folder of your home folder.
4. Finally, register and build `CYTools.jl` as follows:
```julia
    using Pkg
    Pkg.develop(path="path/to/your/CYTools.jl")
    Pkg.build("CYTools")
```


## Documentation

For detailed information about the implemented functionality, please take a look at the most recent [documentation](https://herearound.github.io/CYTools.jl/dev/).


## Bugs and feature requests

If you want to report a bug or request a feature, please do it by raising a [github issue](https://github.com/HereAround/CYTools.jl/issues).


## Contributions

Contributions are highly appreciated. Please notice that:
* Contributions must be done by opening a [pull request](https://github.com/HereAround/CYTools.jl/pulls).
* Pull request must pass a number of checks that are automatically conducted by our test suite, before they can be merged. A further approval by a code owner is appreciated.
* Code is expected to be in agreement with the [Oscar style guide](https://oscar-system.github.io/Oscar.jl/stable/DeveloperDocumentation/styleguide/).


## Contact

This software is work in progress of
* [Martin Bies](https://martinbies.github.io/),
* [Viraf Mehta](https://inspirehep.net/authors/1228975),
* [Andres Rios-Tascon](https://liammcallistergroup.com/author/andres-rios-tascon/).

We use a `slack`-channel for general discussions. If you are interested in joining, please reach out to [Viraf Mehta](https://inspirehep.net/authors/1228975) via  `viraf.mehta@uni-goettingen.de` for details.


## Funding

The work of Martin Bies is supported by SFB-TRR 195 ``Symbolic Tools in Mathematics and their Application of the German Research Foundation (DFG)``.
