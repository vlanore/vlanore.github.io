---
title: Vincent Lanore
layout: default
---

| [Research](index.html)<br/>(thesis, papers, talks...) | [Rest of CV](cv.html)<br/>(formation, teaching...) | [Software development](soft.html)<br/>(projects, skills) | [Contact](contact.html)<br/>(contact info)

# Software
* TOC
{:toc}

## Main software projects

## Bayes toolbox ([link](https://github.com/vlanore/bayes_toolbox))

**Bayes toolbox** is a C++14 header-only library for high-performance Bayesian inference that enables low-level optimizations.
Data types are kept as simple as possible (e.g. structs with raw ` double` members) but the library provides powerful polymorphic operations on those datatypes.
Polymorphism is obtained at compile-time with template metaprogramming to minimize runtime overhead.

Here is a small example of what can be done with the library:
```cpp
// simple graphical model
auto alpha = make_node<exponential>(1.0);
auto mu = make_node<exponential>(1.0);
auto lambda = make_node_array<gamma_ss>(5, n_to_one(alpha), n_to_one(mu)); //node array

auto gen = make_generator(); // random generator
draw(alpha, gen); // draw in distribution
draw(mu, gen);
draw(lambda, gen); // draws whole array
double my_logprob = logprob(alpha) + logprob(mu) + logprob(lambda);
```


### Tinycompo ([link](https://github.com/vlanore/tinycompo))

**Tinycompo** is a component-based framework embedded in C++. It proposes to describe applications as assemblies of software units called *components*.
Contrary to existing component-based frameworks, tinycompo assemblies can be written directly in C++.
Tinycompo leverages C++11 features to provide a syntax as close as possible to a declarative assembly description language.

Here is a hello world tinycompo program:
```c++
#include "tinycompo.hpp"
#include <iostream>

class HelloComponent : public tc::Component {
  public:
    /* declare a port in the constructor */
    HelloComponent() { port("hello", &HelloComponent::hello); } 
    void hello() { std::cout << "Hello world\n"; }
}

int main() {
    tc::Model model; /* declaring an empty assembly model */
    model.component<HelloComponent>("mycompo"); /* adding hello component */

    tc::Assembly assembly(model); /* instantiating assembly */
    assembly.call("hello", "mycompo"); /* calling the hello method */
}
```

Tinycompo was presented in more details in [this journal article](files/cise.pdf).

### CompoGM ([link](https://github.com/vlanore/compoGM))

**CompoGM** is a component-based Bayesian inference library that uses tinycompo.
It proposes to build high performance Bayesian inference applications by assembling pre-made building blocks.
It is based on the *graphical model* representation to specify probabilistic models.
It implements several automatic or semi-automatic performance optimizations from the literature.

Here is an example model specified using CompoGM:

```c++
struct M0 : public Composite {
    static void contents(Model& m, IndexSet& experiments, IndexSet& samples,
                         map<string, map<string, int>>& data) {
        m.component<OrphanExp>("alpha", 1, 1);
        m.component<OrphanExp>("mu", 1, 1);

        m.component<Array<Gamma>>("lambda", experiments, 1)
            .connect<ArrayToValue>("a", "alpha")
            .connect<ArrayToValue>("b", "mu");

        m.component<Matrix<Poisson>>("K", experiments, samples, 0)
            .connect<MatrixLinesToValueArray>("a", "lambda")
            .connect<SetMatrix<int>>("x", data);
    }
};
```

CompoGM was presented in more details in [this journal article](files/cise.pdf).

### Bayescode ([link](https://github.com/bayesiancook/bayescode))

I'm a contributor to **bayescode** which was initially written by *Nicolas Lartillot*.
It is a collection of large-scale C++/MPI sequence analysis programs that use codon models and Bayesian inference.
Along with *Bastien Boussau*, *Philippe Veber* and *Thibault Latrille*, we have endeavored to heavily refactor this code so that the development of new methods would be easier.

Notable methods in bayescode include **diffsel**, a tool to detect adaptive convergent amino acid evolution.
A multigene version of diffsel is currently being optimized for use on [supercomputer occigen](https://www.cines.fr/calcul/materiels/occigen/).

### Convergence method evaluation pipeline ([link](https://gitlab.in2p3.fr/pveber/reviewphiltrans))

I co-wrote a **pipeline to evaluate convergence detection methods** along with *Carine Rey* and *Philippe Veber*.
This pipeline is meant to run existing convergence detection methods from the literature and compare their results on simulated data.
It is written in OCaml using the [bistro](https://github.com/pveber/bistro) workflow framework.

A review of existing convergence detection methods was conducted using this pipeline. Results can be seen in [this paper](https://www.biorxiv.org/content/early/2019/01/07/513010).
