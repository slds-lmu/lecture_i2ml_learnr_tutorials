# Introduction to Machine Learning - Interactive Tutorials

This repository contains the [`learnr`](https://rstudio.github.io/learnr/index.html) tutorials for the lecture ["Introduction to machine learning"](https://github.com/compstat-lmu/lecture_i2ml).

Each day is treated interactively in form of a Shiny App.

## Run Locally

To run a tutorial locally the only thing you have to do is to run `rmarkdown::run("tutorial.Rmd")` of the specific chapter. For instance, to run the ml-basics chapter you just have to call:
```r
rmarkdown::run("ml-basics/tutorial-ml-basics.Rmd")
```

**NOTE:** It seems that the app is not correctly loaded when calling `run` from the terminal. Opening the `tutorial.Rmd` in RStudio and clicking the `Run document` will properly build the app.

**NOTE:** `learnr` saves the state of all tutorials in `file.path(rappdirs::user_data_dir(), "R", "learnr", "tutorial", "storage")`, if you are developing, delete this every time before you re-run the app for testing:
Just do `unlink(file.path(rappdirs::user_data_dir(), "R", "learnr", "tutorial", "storage"))`.


## Run on shinyapps.io

## Check results

Since `lreanr` passes the defined objects from the student directly as `R` environment it is possible to use any checking or testing mechanism we like. There are two packages that are very suitable for that task:

-   `testthat`: http://testthat.r-lib.org/
-   `testwhat`: https://datacamp.github.io/testwhat/index.html

### testthat

> Testing your code can be painful and tedious, but it greatly increases the quality of your code. testthat tries to make testing as fun as possible, so that you get a visceral satisfaction from writing tests.

### testwhat

> Verify R code submissions and auto-generate meaningful feedback messages. Originally developed for R exercises on DataCamp for so-called Submission Correctness Tests, but can also be used independently.

Using `testwhat` might be very useful in terms of parsing the submitted and solution code and checking multiple things like objects, functions, function definitions, and so on.
