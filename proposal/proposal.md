Project proposal
================
THE Triangle

``` r
library(tidyverse)
library(readxl)
library(janitor)
library(broom)
```

## 1. Introduction

Microplastics have become more and more well known throughout the world
in the past few years. We now recognize that they are an incredibly
dangerous bi-product to marine life and many organizations have begun to
attack the problem. That is what this project is about

## 2. Data

Our project will be looking at a 2023 dataset by Leslie Hart of
microplastic samples in prey fish caught in Sarasota Bay. The samples
were extracted from muscle tissue and GI tracts of the fish, and sorted
by size, type, color, and quantity.

``` r
fish_microplastics <- read_xlsx("../data/Fish_Microplastics_Data_Repository.xlsx", 
                                na = "NA") %>%
  janitor::clean_names() 

fish_microplastics <- fish_microplastics %>%
  mutate(sieve_size = str_extract(sieve_size, pattern = "[:digit:]+")) %>%
  mutate(sieve_size = case_when(sieve_size == "LG" ~ 777,
          TRUE ~ as.numeric(sieve_size))) %>%
  mutate(hot_needle = case_when(hot_needle == "yes" ~ TRUE, hot_needle == "no" ~ FALSE))
```

``` r
glimpse(fish_microplastics)
```

    ## Rows: 420
    ## Columns: 16
    ## $ sample_batch                 <chr> "Sept 2022", "Sept 2022", "Sept 2022", "S…
    ## $ fish_id                      <chr> "Oc 31", "Oc 31", "Oc 31", "Oc 31", "Oc 3…
    ## $ sieve_size                   <dbl> NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, N…
    ## $ number_fractions             <dbl> 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,…
    ## $ sample_label                 <chr> "Oc_31_11142_201022_F", "Oc_31_11142_2010…
    ## $ sample_type                  <chr> "Fish Muscle", "Fish Muscle", "Fish Muscl…
    ## $ net_sample_mass_g            <dbl> 9.7, 9.7, 9.7, 9.7, 9.7, 9.7, 9.7, 9.7, 9…
    ## $ dissection_collection_date   <dttm> 2022-10-20, 2022-10-20, 2022-10-20, 2022…
    ## $ dissection_or_field_blank_id <chr> "Dissection_blank_201022_MP", "Dissection…
    ## $ digestion_blank_id           <chr> "Digestion_blank_102022", "Digestion_blan…
    ## $ particle_type                <chr> "Fiber_single", "Fiber_single", "Fiber_si…
    ## $ color                        <chr> "black", "transparent", "red", "yellow", …
    ## $ quantity                     <dbl> 3, 19, 19, 40, 5, 1, 12, 11, 10, 2, 2, 2,…
    ## $ hot_needle                   <lgl> TRUE, TRUE, TRUE, TRUE, TRUE, TRUE, TRUE,…
    ## $ collection_lat               <dbl> 27.42136, 27.42136, 27.42136, 27.42136, 2…
    ## $ collection_long              <dbl> -82.64988, -82.64988, -82.64988, -82.6498…

## 3. Ethics review

We did not collect this data so there was no ethical issue of us cutting
up the fish.

## 4. Data analysis plan

With the data we plan on plotting it in a spatial manner. We want to see
where these fish were gathered and if there is any correlation. We also
want to see if there is a correlation between different fish and the
average count of micro plastics found within it. It would be interesting
to see if multiple variables like the distinct IDs and the average count
have any correlation.
