# csurvey-data

This repository contains external data files used in examples and illustrations
for the **csurvey** R package.

The main data sets are subsets of the National Survey of College Graduates (NSCG):

- `nscg19.rda`
- `nscg19_2.rda`

These files are stored via **Git LFS** because of their size and are **not**
distributed with the `csurvey` package on CRAN.

## Usage

To reproduce the NSCG examples from the csurvey vignette or paper, you can
download the `.rda` files directly from this repository and load them in R:

```r
url1 <- "https://github.com/xliaosdsu/csurvey-data/raw/main/nscg19.rda"
url2 <- "https://github.com/xliaosdsu/csurvey-data/raw/main/nscg19_2.rda"

dest1 <- tempfile(fileext = ".rda")
dest2 <- tempfile(fileext = ".rda")

download.file(url1, destfile = dest1, mode = "wb")
download.file(url2, destfile = dest2, mode = "wb")

load(dest1)  # loads nscg19
load(dest2)  # loads nscg19_2
```
