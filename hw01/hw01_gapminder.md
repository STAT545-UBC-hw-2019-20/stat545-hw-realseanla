STAT 545 - Assignment 1.2
================
Sean La
09/09/2019

First, we’ll load the Gapminder datatset.

``` r
library(gapminder)
gapminder.df <- gapminder
```

Let’s look at some of the columns of this dataset…

``` r
names(gapminder.df)[1:4]
```

    ## [1] "country"   "continent" "year"      "lifeExp"

There’s a column called `lifeExp`, which stands for life expectancy.
Let’s find out what the mean and standard deviations for life
expectancy are\!

``` r
life_exp_mean <- mean(gapminder.df$lifeExp)
print(paste('Mean life expectancy is',life_exp_mean,'.'))
```

    ## [1] "Mean life expectancy is 59.4744393661972 ."

``` r
life_exp_sd <- sd(gapminder.df$lifeExp)
print(paste('Standard deviation for life expectancy is',
            life_exp_sd,'.'))
```

    ## [1] "Standard deviation for life expectancy is 12.9171074152412 ."

Let’s make a histogram of the life expectancies to visualize the data
better.

``` r
hist(gapminder.df$lifeExp)
```

![](hw01_gapminder_files/figure-gfm/lifeExp_hist-1.png)<!-- -->
