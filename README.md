
<!-- README.md is generated from README.Rmd. Please edit that file -->

# ondisc-data

This package contains data for use in examples and vignettes of the
`ondisc` package. All datasets are single-cell datasets, stored in HDF5
(.h5), matrix market (.mtx), ondisc (.odm), or R object (.rds) format.

## Installation

Install the package from Github via the following command:

``` r
# install.packages("devtools")
devtools::install_github("katsevich-lab/ondiscdata")
```

## Data overview

The tree structure of the data directory is as follows:

    ├── h5_list
    │   ├── batch-1_1.h5
    │   ├── batch-1_2.h5
    │   └── batch_2-1.h5
    ├── mtx
    │   ├── barcodes.tsv
    │   ├── genes.tsv
    │   └── matrix.mtx
    ├── mtx_list
    │   ├── mtx_dir1
    │   │   ├── barcodes.tsv
    │   │   ├── features.tsv
    │   │   └── matrix.mtx
    │   ├── mtx_dir2
    │   │   ├── barcodes.tsv
    │   │   ├── features.tsv
    │   │   └── matrix.mtx
    │   └── mtx_dir3
    │       ├── barcodes.tsv
    │       ├── features.tsv
    │       └── matrix.mtx
    ├── odm
    │   ├── gene
    │   │   ├── matrix.odm
    │   │   └── metadata.rds
    │   ├── grna_assignment
    │   │   ├── matrix.odm
    │   │   └── metadata.rds
    │   └── grna_expression
    │       ├── matrix.odm
    │       └── metadata.rds
    └── r_matrix
        ├── gene
        │   ├── barcodes.rds
        │   ├── features.rds
        │   └── matrix.rds
        ├── grna_assignment
        │   ├── barcodes.rds
        │   ├── features.rds
        │   └── matrix.rds
        └── grna_expression
            ├── barcodes.rds
            ├── features.rds
            └── matrix.rds

## Accessing the data

To get the file path of a given file, use the system.file command. For
example, to get the full file path of `mtx/matrix.mtx`, use

    system.file("extdata", "mtx/matrix.mtx", package = "ondiscdata")

To access `h5_list/batch-1_1.h5`, use

    system.file("extdata", "h5_list/batch-1_1.h5", package = "ondiscdata")

## Data sources

1.  Xie, Shiqi, et al. “Global analysis of enhancer targets reveals
    convergent enhancer-driven regulatory modules.” Cell reports 29.9
    (2019): 2570-2578. [Raw data
    link](https://www.ncbi.nlm.nih.gov/geo/download/?acc=GSE129837).

2.  500 Human PBMCs, 3’ LT v3.1, Chromium X. Single Cell Gene Expression
    Dataset by Cell Ranger 6.1.0. [Raw data
    link](https://www.10xgenomics.com/resources/datasets/500-human-pbm-cs-3-lt-v-3-1-chromium-x-3-1-standard-6-1-0).

3.  Gasperini, Molly, et al. “A genome-wide framework for mapping gene
    regulation via cellular genetic screens.” Cell 176.1-2 (2019):
    377-390. [Raw data
    link](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE120861)

------------------------------------------------------------------------

[Tim Barry](https://github.com/timothy-barry)
