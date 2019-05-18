# capstone

The goal of capstone is to provide functions for handling earthquake records from 
the National Centers for Environmental Information, National Oceanic and 
Atmospheric Administration's (NOAA) - Significant Earthquake Database. 


## Installation

You can install capstone from github with:


``` r
# install.packages("devtools")
devtools::install_github("Liddlle/capstone")
```

## Example

With this package you can build beautiful leaflet maps such as this:

``` r
load(system.file("data/df.rda", package = "capstone"))

df_clean = eq_clean_data(df)

df_clean %>%
  dplyr::filter(COUNTRY == "MEXICO" & lubridate::year(DATE) >= 2000) %>%
  eq_map(annot_col = "DATE")
```
