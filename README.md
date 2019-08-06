# MANO method for ABCD system
This repository contains all the code and data to regenerate results from our paper:
"High-throughput functional evaluation method for variants of unknown significance in BRCA2"

# Supplementary Code
> M. Ikegami et al., "High-throughput functional evaluation method for variants of unknown significance in BRCA2", in submission. 

## Contents

- [Overview](#overview)
- [Repo Contents](#repo-contents)
- [System Requirements](#system-requirements)
- [Instructions for Use](#instructions-for-use)

# Overview

We developed a high-throughput functional assay based on the mixed-all-nominated-in-one (MANO) method for variants of unknown significance in BRCA2 gene. For analyzing the huge data generated by next-generation sequencing technique, we programmed a Bayesian interference model based on 'VarCall'. It provides a framework for interpretation of variants' pathogenicity, with or without appropriate prior probability.

# Repo Contents

- [summary](./R): summary pdf file and `R` markdown code.
- [sources](./sources): data sources for reproducing the figures.
- [figures](./man): `R` source codes and output figures.

# System Requirements

## Hardware Requirements

The scripts requires only a standard computer with enough RAM to support the operations defined by a user. For minimal performance, this will be a computer with about 8 GB of RAM. For optimal performance, we recommend a computer with the following specs:

RAM: 32+ GB  
CPU: 4+ cores, 4.2+ GHz/core

The runtimes below are generated using a computer with the recommended specs (32 GB RAM, 4 cores@4.2 GHz) and internet of speed 100 Mbps.

## Software Requirements

### `R` and Rstan

This script files runs on `R` and Rstan for Windows, Mac, or Linux, which requires the R version 3.4.0 or later. For install instructions, visit the RStan Getting Started website at
https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started 


### Package dependencies

Users should install the following packages prior to use the scripts, from an `R` terminal:

```
install.packages(c('ggplot2', 'reshape2', 'ggmcmc', 'rstan', 'mclust', 'tidyverse', 'ggsci', 'pROC', 'car', 'shinystan'))
```

which will install in about 5 minutes on a recommended machine.

### Package Versions

This  with all packages in their latest versions as they appear on `CRAN` on April 13, 2019. Users can check [CRAN snapshot](https://mran.microsoft.com/timemachine/) for details. The versions of software are, specifically:

```
"ggplot2 version: 3.1.0"
"ggmcmc version: 1.2"
"rstan version: 2.18.2"
"mclust version: 5.4.3"
"tidyverse version: 1.2.1"
"reshape2 version: 1.4.3"
"ggsci version: 2.9"
"pROC version: 1.14.0"
"car version: 3.0.2"
"shinystan version: 2.5.0"
```

If you are having an issue that you believe to be tied to software versioning issues, please drop us an [Issue](https://github.com/neurodata/mgc/issues). 

# Instructions for Use

Please put all the files in the same directory, and set the working directory appropriately.

# Reproducibility

All the code and data are available in MANO-summary.Rmd and `sourcess` directory to reproduce figures and tables in our paper. Each Bayesian interference takes about 10-20 minutes on a recommended machine.

MANO.pdf generated from MANO.Rmd includes all scripts with information.

```
├── README.md
├── LICENSE
├── summary
│   ├── MANO-summary.pdf
│   └── MANO-summary.Rmd
├── sources
      ├── read_summary.csv
      ├── data_HMC.csv
      └── RT-PCR.csv

2 directories, 7 files
```
