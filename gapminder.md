Gapminder Exercise Template
================
Bora Jin
2018-08-20

## Load packages

``` r
library(tidyverse)
```

## Load data

``` r
gap <- read_csv("https://bit.ly/gap_data")
```

    ## Parsed with column specification:
    ## cols(
    ##   country = col_character(),
    ##   continent = col_character(),
    ##   year = col_integer(),
    ##   lifeExp = col_double(),
    ##   pop = col_double(),
    ##   gdpPercap = col_double()
    ## )

``` r
x = 2
x^3
```

    ## [1] 8

## Exercises

### Exercise 1

How many observations are in this dataset?

There are 1363 observations in the dataset.

### Exercise 2

Visualize the relationship between GDP and life expectancy for countries
in Europe in 1952 using a scatter plot.

![](gapminder_files/figure-gfm/eu_52-1.png)<!-- -->

### Exercise 3

Add year 1967 in another
color.

``` r
eu_52_67 = gap %>% filter(continent == "Europe", year %in% c(1952, 1967))
ggplot(data = eu_52_67, aes(x = gdpPercap, y = lifeExp, colour=factor(year)))+geom_point()
```

![](gapminder_files/figure-gfm/eu_52_67-1.png)<!-- --> add new line
