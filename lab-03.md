Lab 03 - Nobel laureates
================
Lindsey Wilson
01/26/2023

### Load packages and data

``` r
library(tidyverse) 
```

``` r
nobel <- read_csv("data/nobel.csv")
```

## Exercises

### Exercise 1

The `nobel` dataset has 935 observations and 26 variables:

``` r
# this gives the number of observations we have
nobel %>%
  summarize(n())
```

    ## # A tibble: 1 × 1
    ##   `n()`
    ##   <int>
    ## 1   935

``` r
#and this tells us the names/numbers of our variables
names(nobel)
```

    ##  [1] "id"                    "firstname"             "surname"              
    ##  [4] "year"                  "category"              "affiliation"          
    ##  [7] "city"                  "country"               "born_date"            
    ## [10] "died_date"             "gender"                "born_city"            
    ## [13] "born_country"          "born_country_code"     "died_city"            
    ## [16] "died_country"          "died_country_code"     "overall_motivation"   
    ## [19] "share"                 "motivation"            "born_country_original"
    ## [22] "born_city_original"    "died_country_original" "died_city_original"   
    ## [25] "city_original"         "country_original"

We want to filter this for living people. The code to do that is below.
If we did this right, we. should have 228 observations:

``` r
nobel_living <- nobel %>%
  filter(!is.na(country),
         gender != "org",
         is.na(died_date)
         )

nobel_living %>%
  summarize(n())
```

    ## # A tibble: 1 × 1
    ##   `n()`
    ##   <int>
    ## 1   228

### Exercise 2

Remove this text, and add your answer for Exercise 1 here. Add code
chunks as needed. Don’t forget to label your code chunk. Do not use
spaces in code chunk labels.

### Exercise 3

Remove this text, and add your answer for Exercise 1 here. Add code
chunks as needed. Don’t forget to label your code chunk. Do not use
spaces in code chunk labels.

### Exercise 4

…

### Exercise 5

…

### Exercise 6

…
