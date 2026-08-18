# Combine results from occ calls to a single data.frame

Combine results from occ calls to a single data.frame

## Usage

``` r
occ2df(obj, what = "data")
```

## Arguments

- obj:

  Input from occ, an object of class `occdat`, or an object of class
  `occdatind`, the individual objects from each source within the
  `occdat` class.

- what:

  (character) One of data (default) or all (with metadata)

## Details

This function combines a subset of data from each data provider to a
single data.frame, or metadata plus data if you request `what="all"`.
The single data.frame contains the following columns:

- name - scientific (or common) name

- longitude - decimal degree longitude

- latitude - decimal degree latitude

- prov - data provider

- date - occurrence record date

- key - occurrence record key

## Examples

``` r
if (FALSE) { # \dontrun{
# combine results from output of an occ() call
spnames <- c('Accipiter striatus', 'Setophaga caerulescens',
  'Spinus tristis')
out <- occ(query=spnames, from='gbif', gbifopts=list(hasCoordinate=TRUE),
  limit=10)
occ2df(out)
occ2df(out$gbif)

out <- occ(
  query='Accipiter striatus',
  from=c('gbif','ebird','inat'),
  gbifopts=list(hasCoordinate=TRUE), limit=2)
occ2df(out)
occ2df(out$gbif)

# or combine many results from a single data source
spnames <- c('Accipiter striatus', 'Spinus tristis')
out <- occ(query=spnames, from='gbif', limit=2)
occ2df(out$gbif)
} # }
```
