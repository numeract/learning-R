# R details


## If-Else Statements

### `if` from base R

- fast, but not vectorial
- must receive **only one** value, not a vector
- if returns a value which can be assigned
- always leave a space after `if`

```r
    a <- if (one_logical_condition) value_when_TRUE else value_when_FALSE
```


- nested `if`s require curly brackets

```r
if (one_logical_condition) {
    # do something when condition is TRUE
} else {
    # do something else when condition is FALSE
}
```

### `ifelse` from base R

- vectorized version
- faster than `if` when dealing with a vector
    + https://stackoverflow.com/questions/34005423/is-if-faster-than-ifelse
- treat it as a function

### `dplyr::if_else`

- as `if_else` but can deal with NAs and validates data types and vector lengths



## Multi if statements


### Nested `if`s

- allow for different conditions

```r
if (one_logical_condition) {
    # do something when first condition is TRUE
} else if (second_logical_condition) {
    # do something else when second condition is FALSE (and first is FALSE)
} else {
    # do something when both conditions are FALSE
}
```

### `switch` from base R

- think of it as multi-case `if` based on only one 
- one expression that evaluates to one number or one string
- good practice to have a catch-all case (first unnamed argument)


### `purrr::when`

- think of it as vectorized `if`, with multiple conditions 
- uses formulas which must evaluate to a single value
- good practice to have a catch-all case


### `dplyr::case_when`

- think of it as multi-case `if_else`
- uses formulas which must evaluate to a vector(!)
- good practice to have a catch-all case


## Data Frames

### Row names

Avoid row names in data frames

- Many functions in tidyverse remove them
- Not compatible with database tables
- [other issues](http://www.perfectlyrandom.org/2015/06/16/never-trust-the-row-names-of-a-dataframe-in-R/)


## Functions

### Arguments

- use `match.arg()` to validate function arguments
