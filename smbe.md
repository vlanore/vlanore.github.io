---
title: Vincent Lanore
layout: default
---

# Abstract SMBE 2019

**Detecting convergent amino acid evolution in the presence of mutational biases**

*Carine Rey, Vincent Lanore, Philippe Veber, Laurent Guéguen, Nicolas Lartillot, Marie Sémon, Bastien Boussau*

The evolutionary genomics community has taken an interest in locating so-called “convergent sites”, that is, amino acid positions in the genome linked with convergent phenotypic changes. We have recently conducted a review where we evaluated the capacity of 7 methods from the literature to detect convergent sites in simulated alignments [1]. Our simulations used a mutation-selection model where the convergent phenotype is associated with a change of the direction of selection—in the form of a different amino acid fitness profile—and optionally with a change of the effective population size. These simulations did not take into account other phenomena—such as GC-biased gene conversion (gBGC) or CpG hypermutation—which could hamper convergence detection, either by hiding the signal of legitimate convergent sites or by producing non-convergent parallel substitutions leading to false positives. Some of the most advanced detection methods, based on codon models that distinguish mutations at the DNA level from selection at the amino acid level, may be less sensitive to those biases, but this has never been evaluated on simulations.

Therefore, we have developed more complex simulators which allow us to take into account mutational biases such as gBGC and CpG hypermutation. This extension of our method evaluation pipeline allows us to assess the capacity of such biases to produce convergent-looking substitutions, as detected by existing convergence detection methods. This is an important question to address in order to guide future method developments and to assess our ability to detect sites underlying convergent phenotypes. I will present results on simulated data and will look back on real data results with an updated knowledge of the methods’ weaknesses.

[1] Carine Rey, Vincent Lanore, Philippe Veber, Laurent Gueguen, Nicolas Lartillot, Marie Semon, and Bastien Boussau. "Detecting convergent adaptive amino acid evolution." Philosophical Transactions of the Royal Society B. (2019). 10.1098/rstb.2018-0234
