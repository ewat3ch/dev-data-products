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
--- .class #id 

<style type="text/css">
body {background:grey transparent;
}
</style>

## Slidify

- In this tutorial I am going to show you how to make a presentation just like this one
- I will also show some of the features that can be used in conjunction with slidify (i.e. quizzes and html widgets)
- You can download the current version of this presentation [here](https://github.com/jvcasill/slidify_tutorial/tree/gh-pages), use it as a template and edit as you like
- Or you can follow these instructions to make one of your own

--- .segue bg:grey

# First things first...

--- .class #id

## Install packages

- `Slidify` works in R, so you need to download [that](http://cran.r-project.org) if you haven't yet.
- You also need to make sure you have all of the necessary dependencies installed on your computer
- Open R and copy and paste the following code into the console (you only need to do this once)

```{r, eval=FALSE}
install.packages("devtools")  
install_github('slidify', 'ramnathv')  
install_github('slidifyLibraries', 'ramnathv')
```
