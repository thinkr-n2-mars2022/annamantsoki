
<!-- README.md is generated from README.Rmd. Please edit that file -->

# annamantsoki

<!-- badges: start -->

[![R-CMD-check](https://github.com/thinkr-n2-mars2022/annamantsoki/workflows/R-CMD-check/badge.svg)](https://github.com/thinkr-n2-mars2022/annamantsoki/actions)
<!-- badges: end -->

The goal of annamantsoki is to …

## Installation

You can install the development version of annamantsoki from
[GitHub](https://github.com/) with:

``` r
install.packages("devtools")
#> Installing package into '/usr/local/lib/R/site-library'
#> (as 'lib' is unspecified)
devtools::install_github("thinkr-n2-mars2022/annamantsoki")
#> Downloading GitHub repo thinkr-n2-mars2022/annamantsoki@HEAD
#> 
#> * checking for file ‘/tmp/RtmpZz3lgx/remotes26fdc6ab9e67c/thinkr-n2-mars2022-annamantsoki-a1e27a3/DESCRIPTION’ ... OK
#> * preparing ‘annamantsoki’:
#> * checking DESCRIPTION meta-information ... OK
#> * checking for LF line-endings in source and make files and shell scripts
#> * checking for empty or unneeded directories
#> * building ‘annamantsoki_0.0.0.9000.tar.gz’
#> Installing package into '/usr/local/lib/R/site-library'
#> (as 'lib' is unspecified)
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(annamantsoki)
bmi(mass = 80, height = 1.80)
#> [1] 24.69136
library(dplyr)
#> 
#> Attaching package: 'dplyr'
#> The following objects are masked from 'package:stats':
#> 
#>     filter, lag
#> The following objects are masked from 'package:base':
#> 
#>     intersect, setdiff, setequal, union
data("data_weight")
data_weight %>%
  mutate(bmi = bmi(mass = mass, height = height))
#> # A tibble: 87 × 4
#>    name               height  mass   bmi
#>    <chr>               <dbl> <dbl> <dbl>
#>  1 Luke Skywalker       1.72    77  26.0
#>  2 C-3PO                1.67    75  26.9
#>  3 R2-D2                0.96    32  34.7
#>  4 Darth Vader          2.02   136  33.3
#>  5 Leia Organa          1.5     49  21.8
#>  6 Owen Lars            1.78   120  37.9
#>  7 Beru Whitesun lars   1.65    75  27.5
#>  8 R5-D4                0.97    32  34.0
#>  9 Biggs Darklighter    1.83    84  25.1
#> 10 Obi-Wan Kenobi       1.82    77  23.2
#> # … with 77 more rows
```
