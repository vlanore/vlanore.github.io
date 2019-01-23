---
title: Vincent Lanore
layout: default
---

| [Research](index.html)<br/>(thesis, papers, talks...) | [Rest of CV](cv.html)<br/>(formation, teaching...) | [Software development](soft.html)<br/>(projects, skills) | [Contact](contact.html)<br/>(contact info)

# Software
* TOC
{:toc}

## Main software projects

### tinycompo

Repository: [github link](https://github.com/vlanore/tinycompo)

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
    model.component<HelloComponent>("mycompo"); /* adding our hello component */

    tc::Assembly assembly(model); /* instantiating assembly */
    assembly.call("hello", "mycompo"); /* calling the hello method */
}
```

### compoGM

Repository: [github link](https://github.com/vlanore/compoGM)

**CompoGM** is a component-based Bayesian inference library that uses tinycompo.
It proposes to build high performance Bayesian inference applications by assembling pre-made building blocks.
It is based on the *graphical model* representation to specify probabilistic models.
It implements several automatic or semi-automatic performance optimizations from the literature.

Here is an example model specified using CompoGM:

```c++
struct M0 : public Composite {
    static void contents(
        Model& m, IndexSet& experiments, IndexSet& samples, map<string, map<string, int>>& data) {
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

### bayescode

### diffsel

### Convergence detection pipeline 

## Other software

## Technological skills

Languages

parallelization / large scale