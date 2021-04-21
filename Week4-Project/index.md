---
title       : Diamonds Are Forever
subtitle    : Exploring Diamonds Dataset
author      : Ewa Wesolowska
job         : Coursera Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, quiz, bootstrap]  # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
--- 

<style>
article p {
  font-size: 16px;
}
article code {
  font-size: 14px;
}

</style>

### The diamonds dataset

The 'Diamonds are Forever' application explore diamond dataset available with R Package ggplot2.
The dataset contains the price, cut, carat and other attributes of almost 54,000 diamonds.
Built using slidify and hosted on [Diamonds Are Forever](https://ewat3ch.shinyapps.io/diamonds_are_forever/): Application Access


```r
library(ggplot2)
str(diamonds)
```

```
## tibble[,10] [53,940 × 10] (S3: tbl_df/tbl/data.frame)
##  $ carat  : num [1:53940] 0.23 0.21 0.23 0.29 0.31 0.24 0.24 0.26 0.22 0.23 ...
##  $ cut    : Ord.factor w/ 5 levels "Fair"<"Good"<..: 5 4 2 4 2 3 3 3 1 3 ...
##  $ color  : Ord.factor w/ 7 levels "D"<"E"<"F"<"G"<..: 2 2 2 6 7 7 6 5 2 5 ...
##  $ clarity: Ord.factor w/ 8 levels "I1"<"SI2"<"SI1"<..: 2 3 5 4 2 6 7 3 4 5 ...
##  $ depth  : num [1:53940] 61.5 59.8 56.9 62.4 63.3 62.8 62.3 61.9 65.1 59.4 ...
##  $ table  : num [1:53940] 55 61 65 58 58 57 57 55 61 61 ...
##  $ price  : int [1:53940] 326 326 327 334 335 336 336 337 337 338 ...
##  $ x      : num [1:53940] 3.95 3.89 4.05 4.2 4.34 3.94 3.95 4.07 3.87 4 ...
##  $ y      : num [1:53940] 3.98 3.84 4.07 4.23 4.35 3.96 3.98 4.11 3.78 4.05 ...
##  $ z      : num [1:53940] 2.43 2.31 2.31 2.63 2.75 2.48 2.47 2.53 2.49 2.39 ...
```

--- .ninety

### What carat value diamond I can get ?

Having chosen price range, cut quality and clarity, application will plot available diamonds carat avaiable within those parameters.

<img height='500' width='600' src=img-week3/diamonds_are_forever.png>

---  &checkbox

### Quizz



James is planning to ask his girfriend, Linda  to marry him. He would like to buy Linda a diamond ring.
Having `$2,500` in his saving account, can James still buy an 'Ideal' diamond?

Diamond price range from lowest `$326` to `$18,823`, with quality of the cut from Fair, Good, Very Good, Premium to best as Ideal.

1. _Yes_
2. No

*** .hint

Does carat matter ?

*** .explanation

#YES! but with it will be low carat of 0.437 being 5.01 highest in the diamond dataset.

--- &twocol

### How many diamonds available under `$2500` dollar mark ?

*** =left

```r
ggplot(data = diamonds_2500_price) + 
  geom_bar(mapping = aes(x = cut, fill = clarity), 
           position = "dodge")
```

<img src="assets/fig/unnamed-chunk-3-1.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" style="display: block; margin: auto auto auto 0;" />
***=right


```r
ggplot(diamonds_2500_price, 
       aes(carat, price, color=clarity)) + 
       geom_point() 
```

<img src="assets/fig/unnamed-chunk-4-1.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" style="display: block; margin: auto 0 auto auto;" />

*** =fullwidth
