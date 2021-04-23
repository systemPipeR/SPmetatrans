# SPmetatrans 

<!-- badges: start -->
[![R-CMD-check](https://github.com/systemPipeR/SPmetatrans/actions/workflows/R_CMD.yml/badge.svg)](https://github.com/systemPipeR/SPmetatrans/actions/workflows/R_CMD.yml)
[![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
<!-- badges: end -->

> This pipeline is currently under development and does not have a stable release yet.

## Introduction

#### Installation 

To install the package, please use the _`BiocManager::install`_ command:
```
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::install("systemPipeR/SPmetatrans", build_vignettes=TRUE, dependencies=TRUE)
```
To obtain the *systemPipeR* and *systemPipeRdata*, please run as follow:
```
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::install("systemPipeR")
BiocManager::install("systemPipeRdata")
```

## Workflow environment

Workflow includes following steps:

1. Read preprocessing
    + Quality filtering (trimming)
    + FASTQ quality report
2. Filter reads by taxon (i.e. remove unwanted organisms) or use all data
3. *de novo* assembly or genome-guided assembly
4. Read count normalization on global scale or re-scaled from organism-level normalization
5. Annotation
6. Differential expression gene or transcript analysis
