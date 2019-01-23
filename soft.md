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
**Tinycompo** is a component-based framework embedded in C++. It proposes to describe applications as assemblies of software units called *components*.
Contrary to existing component-based frameworks, tinycompo assemblies can be written directly in C++.
Tinycompo leverages C++11 features to provide a syntax as close as possible to a declarative assembly description language.

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

### bayescode

### diffsel

### Convergence detection pipeline 

## Other software

## Technological skills

Languages

parallelization / large scale