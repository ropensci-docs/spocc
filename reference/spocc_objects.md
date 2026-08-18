# spocc objects and their print, plot, and summary methods

spocc objects and their print, plot, and summary methods

## Usage

``` r
# S3 method for class 'occdat'
print(x, ...)

# S3 method for class 'occdatind'
print(x, ...)

# S3 method for class 'occdat'
summary(object, ...)

# S3 method for class 'occdatind'
summary(object, ...)

# S3 method for class 'occnames'
print(x, ...)
```

## Arguments

- x:

  Input, of class occdatind

- ...:

  Further args to print, plot or summary methods

- object:

  Input to summary methods

## See also

Other queries:
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md),
[`occ_names()`](https://docs.ropensci.org/spocc/reference/occ_names.md),
[`occ_names_options()`](https://docs.ropensci.org/spocc/reference/occ_names_options.md),
[`occ_options()`](https://docs.ropensci.org/spocc/reference/occ_options.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# occdat object
res <- occ(query = 'Accipiter striatus', from = 'gbif')
res
print(res)
class(res)

# occdatind object
res$gbif
print(res$gbif)
class(res$gbif)

# print summary of occdat object
summary(res)

# print summary of occdatind object
summary(res$gbif)

# Geometry based searches print slightly differently
bounds <- c(-120, 40, -100, 45)
(res <- occ(from = "idigbio", geometry = bounds, limit = 10))
res$idigbio
## Many bounding boxes/WKT strings
bounds <- list(c(165,-53,180,-29), c(-180,-53,-175,-29))
res <- occ(from = "idigbio", geometry = bounds, limit = 10)
res$idigbio
} # }
```
