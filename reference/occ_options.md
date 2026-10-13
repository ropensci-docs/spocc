# Look up options for parameters passed to each source

Look up options for parameters passed to each source

## Usage

``` r
occ_options(from = "gbif", where = "console")
```

## Arguments

- from:

  (character) Data source to get data from, any combination of gbif,
  ebird, idigibio and/or vertnet. Case doesn't matter. inat is not
  included here, see that package's help docs.

- where:

  (character) One of console (print to console) or html (opens help
  page, if in non-interactive R session, prints help to console).

## Value

Opens up the documentation for the function that is used internally
within the occ function for each source.

## Details

Any of the parameters passed to e.g.
[`rgbif::occ_data()`](https://docs.ropensci.org/rgbif/reference/occ_data.html)
from the `rgbif` package can be passed in the associated gbifopts list
in [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md)

Note that the from parameter is lowercased within the function and is
called through match.arg first, so you can match on unique partial
strings too (e.g., 'rv' for 'rvertnet').

## See also

Other queries:
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md),
[`occ_names()`](https://docs.ropensci.org/spocc/reference/occ_names.md),
[`occ_names_options()`](https://docs.ropensci.org/spocc/reference/occ_names_options.md),
[`spocc_objects`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# opens up documentation for this function
occ_options()

# Open up documentation for the appropriate search function for each source
occ_options('gbif')
occ_options('ebird')
occ_options('idigbio')
occ_options('vertnet')

# Or open in html version
occ_options('gbif', 'html')
} # }
```
