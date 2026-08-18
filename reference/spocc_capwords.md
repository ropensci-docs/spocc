# Capitalize the first letter of a character string.

Capitalize the first letter of a character string.

## Usage

``` r
spocc_capwords(s, strict = FALSE, onlyfirst = FALSE)
```

## Arguments

- s:

  A character string

- strict:

  Should the algorithm be strict about capitalizing. Default: `FALSE`

- onlyfirst:

  Capitalize only first word, lowercase all others. Useful for taxonomic
  names.

## Examples

``` r
if (FALSE) { # \dontrun{
spocc_capwords(c('using AIC for model selection'))
spocc_capwords(c('using AIC for model selection'), strict=TRUE)
} # }
```
