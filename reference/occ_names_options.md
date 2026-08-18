# Look up options for parameters passed to each source for occ_names function

Look up options for parameters passed to each source for occ_names
function

## Usage

``` r
occ_names_options(from = "gbif", where = "console")
```

## Arguments

- from:

  (character) Data source to get data from, only gbif. Case doesn't
  matter.

- where:

  (character) One of console (print to console) or html (opens help
  page, if in non-interactive R session, prints help to console).

## Value

Opens up the documentation for the function that is used internally
within the occ function for each source.

## Details

Any of the parameters passed to e.g.
[`rgbif::name_lookup()`](https://docs.ropensci.org/rgbif/reference/name_lookup.html)
from the `rgbif` package can be passed in the associated gbifopts list
in [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md).

Note that the from parameter is lowercased within the function and is
called through `match.arg` first, so you can match on unique partial
strings too (e.g., 'rg' for 'rgbif').

## See also

Other queries:
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md),
[`occ_names()`](https://docs.ropensci.org/spocc/reference/occ_names.md),
[`occ_options()`](https://docs.ropensci.org/spocc/reference/occ_options.md),
[`spocc_objects`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# opens up documentation for this function
occ_names_options()

# Open up documentation for the appropriate search function for each source
occ_names_options('gbif')

# Or open in html version
occ_names_options('gbif', 'html')
} # }
```
