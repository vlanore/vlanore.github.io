---
title: Vincent Lanore
layout: default
---

| [Research](index.html)<br/>(thesis, papers, talks...) | [Rest of CV](cv.html)<br/>(formation, teaching...) | [Software development](soft.html)<br/>(projects, skills) | [Contact](contact.html)<br/>(contact info)

# Research
* TOC
{:toc}

## Current situation

**Temporary researcher** (CDD chercheur) at CNRS in ["Le Cocon" team](https://lbbe.univ-lyon1.fr/-Equipe-Le-Cocon-.html) at [LBBE](https://lbbe.univ-lyon1.fr/).<br/>
Working on comparative genomics, high-performance bayesian inference and software engineering for high-performance bioinformatics.<br/>
Work done in the context of the [convergenomix](http://lbbe.univ-lyon1.fr/convergenomix/) ANR project.<br/>
Started on 2016/11/01.

## Thesis

**On Scalable Reconfigurable Component Models for HPC**<br/>
(*Modèles à composants reconfigurables et passant à l'échelle pour le calcul haute performance*)<br/>
Under the direction of Christian Pérez<br/>
LIP laboratory, [AVALON team](https://www.inria.fr/en/teams/avalon), funded by ENS de Lyon<br/>
Starting date: 2012/10/01, defended on 2015/12/10<br/>
[Full text on theses.fr](http://www.theses.fr/2015ENSL1051)

### Jury
* Mr Raymond Namyst, professor, Univ. of Bordeaux, president
* Mr Marco Danelutto, associate professor, Univ. of Pisa, reviewer
* Ms Laurence Duchien, professor, Univ. of Lille 1, examiner
* Mr Laxmikant V. Kale, professor, Univ. of Illinois, examiner
* Mr Christian Perez, senior researcher, Inria, thesis director
* Mr Jean-Bernard Stefani, senior researcher, Inria, reviewer and examiner

### Abstract
Component-based programming is a programming paradigm which eases code reuse and separation of concerns. Some component models, which are said to be "reconfigurable", allow the modification at runtime of an application's structure. However, these models are not suited to High-Performance Computing (HPC) as they rely on non-scalable mechanisms.

The goal of this thesis is to provide models, algorithms and tools to ease the development of component-based reconfigurable HPC applications.The main contribution of the thesis is the DirectMOD component model which eases development and reuse of distributed transformations. In order to improve on this core model in other directions, we have also proposed:
* the SpecMOD formal component model which allows automatic specialization of hierarchical component assemblies and provides high-level software engineering features;
* mechanisms for efficient fine-grain reconfiguration for AMR applications, an important application class in HPC.

An implementation of DirectMOD, called DirectL2C, as been developed so as to implement a series of benchmarks to evaluate our approach. Experiments on HPC architectures show our approach scales. Moreover, a quantitative analysis of the benchmark's codes show that our approach is compact and eases reuse. 

## Publications

### International Peer-Reviewed Journals

| **Detecting convergent adaptive amino acid evolution**<br/>Rey C., Lanore V., Veber P., Guéguen L., Lartillot N., Sémon M., Boussau B.<br/>Philosophical Transactions of the Royal Society B.<br/>[Full text on BioRxiv](https://www.biorxiv.org/content/early/2019/01/07/513010) |

| **Fostering Reuse in Scientific Computing with Embedded Components: Application to high-performance Bayesian inference for bioinformatics**<br/>Lanore V.<br/>Computing in Science & Engineering (CiSE)  - Special issue on Accelerating Scientific Discovery with Reusable Software.<br/>[Full text](files/cise.pdf) |

### International Peer-Reviewed Conferences

| **A Reconfigurable Component Model for HPC**<br/>Lanore V., Pérez C.<br/>The 18th International ACM Sigsoft Symposium on Component-Based Software Engineering (CBSE'2015)<br/>Montréal: Canada (2015) <br/> [Full text on HAL](https://hal.inria.fr/hal-01120117v1) |

### International Peer-Reviewed Workshops

| **Towards Application Variability Handling with Component Models: 3D-FFT Use Case Study**<br/>Lanore V., Pérez C., Richard J.<br/>The 8th Workshop on UnConventional High Performance Computing (UCHPC'15)<br/>Vienna: Austria (2015) <br/> [Full text on HAL](https://hal.archives-ouvertes.fr/hal-01192732) |

### National Peer-Reviewed Conferences

| **Easing Locking of High-Performance Call-Stack-Based Component Assemblies**<br/>(*Simplifier le verrouillage d’assemblages de composants haute performance à pile d’appel*)<br/>Lanore V.<br/>Conférence en parallélisme, architecture et système (Compas'2015) <br/>Lille: France (2015) <br/> [Full text on HAL](https://hal.archives-ouvertes.fr/hal-01193081) |

| **On Scheduling Multi-level Applications**<br/>(*De l'ordonnancement des applications multi-niveaux*)<br/>Lanore V., Klein C.<br/>Conférence en parallélisme, architecture et système (ComPAS'2013) <br/>Grenoble: France (2013) <br/> [Full text on HAL](http://hal.archives-ouvertes.fr/hal-00764007) |

### Technical Reports and White Papers

| **A Calculus Enabling Reuse and Composition of Component Assembly Specialization Processes**<br/>Lanore V., Pérez C.<br/>Inria Research Report n°8761 (2015) <br/>[Full text on HAL](https://hal.archives-ouvertes.fr/hal-01179483) |

| **Evaluating Component Assembly Specialization for 3D FFT**<br/>Richard J., Lanore V., Pérez C.<br/>PRACE White Paper n°182 (2014) <br/>[Full text](http://www.prace-ri.eu/IMG/pdf/WP182.pdf) |

### Other

| **Towards Reconfigurable HPC Component Models**<br/> Perez C., Lanore V.<br/> International Conference on High Performance Computing & Simulation (HPCS). IEEE, 2018.<br/> Extended abstract for keynote talk by Christian Pérez <br/>[Abstract full text](files/hpcs.pdf) |

## External talks

(Internal team and project talks not listed. Conference talks with associated papers listed above as papers)

| **Detecting convergent amino acid evolution in the presence of mutational biases**<br/>
SMBE Conference <br/>Manchester, <font color="red">planned talk (Jul 22nd)</font><br/>[accepted abstract](smbe.html) |

| **Detecting convergent substitutions with sparse codon-based differential-selection models**<br/>ALPHY conference<br/>Paris, February 8th<br/>[abstract](alphy.html) - [slides](files/alphy.pdf) |

| **Building high-performance bayesian inference applications with software components**<br/>APPLIBUGS Meeting<br/>Lyon, June 21st, 2018<br/> [Slides](http://genome.jouy.inra.fr/applibugs/applibugs.18_06_21.vlanore.pdf) |

| **A Reconfigurable Component Model for HPC**<br/>Ctrl-A seminar presentation<br/>Grenoble, July 18th, 2015<br/>[Slides](files/ctrl-a.pdf) |

| **Towards a Reconfigurable HPC Component Model**<br/>C2S@EXA Meeting<br/>Bordeaux, July 10th, 2014<br/>[Slides](files/cs2exa.pdf) |

| **Static 2D FFT Adaptation Through a Component Model Based on Charm++ (preliminary results)**<br/>9th Workshop of the INRIA-Illinois Joint Laboratory on Petascale Computing<br/>Lyon, June 14th, 2013<br/>[Slides](files/jointlab.pdf) |


## Participation to internship supervision

| **Conception et formalisation d’un mini-langage pour décrire des assemblages complexes à base de graphes**<br/>Maverick Chardet<br/>L3 internship, summer 2015, 2 months |

| **Implémentation et évaluation d’algorithmes parallèles de FFT 3D à base de modèles à composants logiciels**<br/>Jérôme Richard<br/>M2 internship, summer 2014  |
