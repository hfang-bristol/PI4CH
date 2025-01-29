# [An R package `PI4CH`](https://github.com/hfang-bristol/PI4CH)

## @ Overview

> The `PI4CH` is an R package designed to implement the use of Priority Index (PI) in identifying therapeutic candidates (both therapeutic targets and repurposed drugs) based on multi-layered datasets related to age-related clonal hematopoiesis, known as `clonal hematopoiesis (CH)`. `CH` is used to describe the occurrence of somatic mutations in healthy persons without hematologic abnormalities.


## @ Installation

### 1. Install R

Please install R (version 4.4.2 or above); see https://cran.r-project.org

Below describes the instruction how to install R on `Ubuntu` (assuming you have a `ROOT (sudo)` privilege).

```ruby
sudo su
# here enter your password

wget http://www.stats.bris.ac.uk/R/src/base/R-4/R-4.4.2.tar.gz
tar xvfz R-4.4.2.tar.gz
cd ~/R-4.4.2
./configure
make
make check
make install
R # start R
```

### 2. Install R packages

```ruby
R # start R

# if the package 'BiocManager' not installed, please do so
if(!("BiocManager" %in% rownames(installed.packages()))) install.packages("BiocManager")

# first, install basic packages: remotes, tidyverse
BiocManager::install(c('remotes','tidyverse'), dependencies=T)

# then, install the package 'PI4CH' (now hosted at github)
BiocManager::install("hfang-bristol/PI4CH", dependencies=T, force=T)

# check the package 'PI4CH' successfully installed
library(PI4CH)
```


## @ Contact

> Please drop [email](mailto:fh12355@rjh.com.cn) for bug reports or enquiries.


