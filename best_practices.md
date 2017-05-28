# Best practices in R


## Functions

- Try to write *pure functions*
    + Avoid side-effects
    + Receive all arguments in the argument list (do not rely on global values)
    + Return only one data type
- For complex functions, try separating them into pure and not pure
    + For example, dplyr processing is pure, but ggplot-ing is not pure
- For Not pure functions (e.g., commands):
    + Have them return (invisibly) the original input, to facilitate pipelines


## Packages

- Always load them at the beginning of the (main) script
    + if the user does not have all the packages loaded, the script should fail fast
    + in a notebook or in a Rmd file, this is the "setup" chunk
    + if a package is used only with its namespace (e.g., `tidyr::`), list it in the setup chunk as a comment `# library(tidyr)`
- Always use `library()` not `require()`
    + [library() vs require() in R](https://yihui.name/en/2014/07/library-vs-require/)


## Statements

- For if-else, use curly brackets
    ```R
    if (condition) {
        # do something when condition is TRUE
    } else {
        # do something else when condition is FALSE
    }
    ```
