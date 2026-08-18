# Search for species names across many data sources.

Search for species names across many data sources.

## Usage

``` r
occ_names(
  query = NULL,
  from = "gbif",
  limit = 100,
  rank = "species",
  callopts = list(),
  gbifopts = list()
)
```

## Arguments

- query:

  (character) One to many names. Either a scientific name or a common
  name. Only scientific names supported right now.

- from:

  (character) Data source to get data from, only gbif

- limit:

  (numeric) Number of records to return. This is passed across all
  sources. To specify different limits for each source, use the options
  for each source (gbifopts). See Details for more.

- rank:

  (character) Taxonomic rank to limit search space. Used in GBIF.

- callopts:

  Options passed on to
  [`crul::HttpClient()`](https://docs.ropensci.org/crul/reference/HttpClient.html),
  e.g., for debugging curl calls, setting timeouts, etc.

- gbifopts:

  (list) List of named options to pass on to
  [`rgbif::name_lookup()`](https://docs.ropensci.org/rgbif/reference/name_lookup.html).
  See also
  [`occ_names_options()`](https://docs.ropensci.org/spocc/reference/occ_names_options.md)

## Details

Not all 7 data sources available from the
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) function are
available here, as not all of those sources have functionality to search
for names.

We strongly encourage you to use the `taxize` package if you want to
search for taxonomic or common names, convert common to scientific
names, etc. That package was built exactly for that purpose, and we only
provide a bit of name searching here in this function.

## See also

Other queries:
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md),
[`occ_names_options()`](https://docs.ropensci.org/spocc/reference/occ_names_options.md),
[`occ_options()`](https://docs.ropensci.org/spocc/reference/occ_options.md),
[`spocc_objects`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# Single data sources
## gbif
(res <- occ_names(query = 'Accipiter striatus', from = 'gbif'))
head(res$gbif$data[[1]])
} # }
```
