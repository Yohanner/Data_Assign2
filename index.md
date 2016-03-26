---
title       : Coursera
subtitle    : How are you doing in data science courses?
author      : Yohannes R.
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## This page shows you how my app works

- It asks for five of your previous data science specialization courses score
- It calculates the mean of those inputs
- It tells you what your average score is
- It tells you what your expected score is for "Developing data products course"
- It puts a comment depending on your average score

---  .codefont
## How the App. works
##### Suppose you input the following as your scores:
80,70,90,100,100
##### First, it reads the numbers as vectors as follows:

```r
x=c(80,70,90,100,100)
```
##### Then, it calculates your average score as
 
 ```r
 Avg_score=mean(rbind(x), na.rm=TRUE)
 ```

##### It then ouputs your score as 
Your averge score is:
 
 ```
 ## [1] 88
 ```

---
## Continued ...

##### It also gives an expected score:

I would expect your "Developing data products course score to be:"
 
 ```
 ## [1] 88
 ```

##### Finally, a comment based on your average score :)
 
 ```
 ## [1] "Very good"
 ```

---

## Appendix

##### The complete R-code is

- x=c(80,70,90,100,100)

- Avg_score=mean(rbind(x), na.rm=TRUE)

- Avg_score

- ifelse(Avg_score<50, "Not a good score, try harder", ifelse (Avg_score<70,"Not bad, but you can still improve",ifelse(Avg_score<80,"Good",ifelse(Avg_score<90,"Very good","Excellent"))))

Try my App and have fun!

