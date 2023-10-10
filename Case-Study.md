Case Study Assessment
================
10-10-2023

Class Package Library Import

``` r
library(p8105.datasets)
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.3     ✔ readr     2.1.4
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.0
    ## ✔ ggplot2   3.4.3     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.2     ✔ tidyr     1.3.0
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
#Global Markdown Knitting Settings
knitr::opts_chunk$set(
  fig.width = 6,
  fig.asp = .6,
  out.width = "90%"
)

nyc_airbnb = nyc_airbnb |> 
  rename(borough = neighbourhood_group) |> 
  mutate(stars = review_scores_location/2)
```

# Brainstorm Questions

- Where are AirBNBs expensive?
- Borough? Neighborhood?
- Do other factors (room type affect price?) What about rating?
- How long are AirBNBs active?
- Are Air BNBs Illegal and do they shut down?
- Which units have the most availability?
- How is the review socore impacted by location?
- How many apartments are run by one host?
