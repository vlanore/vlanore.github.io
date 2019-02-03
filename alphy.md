---
title: Vincent Lanore
layout: default
---

# Abstract ALPHY 2019

## Detecting convergent substitutions with sparse codon-based differential-selection models

*Vincent Lanore, Bastien Boussau, Philippe Veber, Nicolas Lartillot*

Identifying amino acid substitutions linked with convergent phenotypic changes has recently been a topic of interest in the evolutionary genomics community. A promising approach to this problem, called diffsel, was presented in [1]. This approach belongs to the family of  phylogenetic codon models based on the so-called “mutation-selection” formalism, in which mutations are modeled at the nucleotide level, but fixation probability depends on the fitness of the encoded amino acid. Each site has its own vector of fitness parameters for the 20 amino-acids. On top of that, diffsel changes the site-specific fitness of amino acids on branches leading to species with the convergent phenotype. This is done by adding a “differential selection effect” to the fitness of amino acids along these branches only.

Diffsel implements a Bayesian version of this model, in which amino acid fitnesses and differential effects are evaluated per-site along a tree and alignment. Sites which exhibit significant differential effects are deemed “convergent”. There are two difficulties with the current model. First, determining which differential effects are significant can be difficult. Second, diffsel attempts to precisely evaluate the fitnesses changes of all amino acids at each position, even for those having low fitness, which is not useful and might come at a cost in terms of computation time or statistical power.

Instead, we propose to have only certain of the amino acids at each site with significant fitness—the rest having a low default fitness ε—and among them only some with differential effects. From a Bayesian perspective this makes the model “sparse” in the sense that indicator boolean variables control for each amino acid and each site the complexity of the fitness model—either ε, estimated fitness, or estimated fitness plus differential effect. This approach provides a clear diagnostic of whether a site is convergent in the form of the posterior probability of the differential effect indicators, and simplifies the evaluation of low fitnesses. We compare this “sparse diffsel” approach to regular diffsel and other convergence detection methods on simulations and real datasets.

**[1]** Parto S, Lartillot N. *Molecular adaptation in Rubisco: Discriminating between convergent evolution and positive selection using mechanistic and classical codon models.* PLoS One. 2018 Apr 18;13(4):e0196267.

