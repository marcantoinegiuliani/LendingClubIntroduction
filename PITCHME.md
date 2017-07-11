## Who will be rich ? Who will die in misery ?
##### <span style="font-family:Helvetica Neue; font-weight:bold">A <span style="color:#e49436">Lending Club</span> Introduction to data science</span>

---

## What is the Lending Club

* Funded with 10 million $ in 2007 as one of the first Facebook apps
* Allows peer-to-peer money lending
* Makes 500 million $ in 2016 for almost 9 billion $ of emited loans

---

## What is lending Club

![Image-Absolute](assets/lending_club_description.png)

---

## The challenge

* In this session you will be given an extract of a few already issued loans, and observe if they defaulted. Based on this observation you can decide to fund or not new loans where you do not know if they will default or not.
* Every player has the same starting money
* At the end we compute how much each of you would have make

---

## A tool to scrutinize data : R

* Open source written in C and Fortran
* Comes from S written at Bell Labs by John Chambers
* Re-written by Ihaka and Gentleman in 1992, New Zealand

---

## The Wickham revolution

![Image-Absolute](assets/wickham.jpg)

---

## Loading data

```R
library(tidyverse)
loan_data <- read_csv("loan.csv")
```

---

## dplyr : a grammar of data manipulation

Five verbs to rule them all:
* **filter()**
* **select()**
* **arrange()**
* **mutate()**
* **summarise()**

One adverb **group_by()**.

One idiom : the pipe %>%.

---

## An example

```R
loan_data %>%
  filter(application_type != "JOINT")
```

---

## ggplot2 : a grammar of graphics

> The simple graph has brought more information to the data analyst’s mind than any other device.
>
> -- <cite>John Tukey</cite>

---

## ggplot2 : a grammar of graphics

What is a plot ?

A plot is a mapping from data to aesthetics (coordinates, color, etc ...).

---

## ggplot2 : a grammar of graphics

```R
train_loans %>%
    ggplot(aes(x = grade, y = loan_amnt)) + geom_boxplot()
```

---

