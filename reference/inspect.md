# Get more data on individual occurrences

Fetches the complete record, which may or may not be the same as
requested through
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md). Some data
providers have different ways to retrieve many occurrence records vs.
single occurrence records - and sometimes the results are more verbose
when retrieving a single occurrence record.

## Usage

``` r
inspect(x, from = "gbif")

# S3 method for class 'data.frame'
inspect(x, from = "gbif")

# S3 method for class 'occdat'
inspect(x, from = "gbif")

# S3 method for class 'occkey'
inspect(x, from = "gbif")
```

## Arguments

- x:

  The output from
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) call,
  output from call to
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md), or
  an occurrence ID as a occkey class.

- from:

  (character) The data provider. One of gbif, inat, or vertnet

## Value

A list, with each slot named for the data source, and then within data
sources is a slot for each taxon, named by it's occurrence ID.

## Examples

``` r
if (FALSE) { # \dontrun{
spnames <- c('Accipiter striatus', 'Spinus tristis')
out <- occ(query=spnames, from=c('gbif','idigbio'),
   gbifopts=list(hasCoordinate=TRUE), limit=2)
res <- occ2df(out)
inspect(res)

out <- occ(query=spnames, from='gbif', gbifopts=list(hasCoordinate=TRUE),
  limit=4)
res <- occ2df(out)
inspect(res)

# from occkeys
key <- as.gbif(res$key[1])
inspect(key)

# idigbio
spnames <- c('Accipiter striatus', 'Spinus tristis')
out <- occ(query=spnames, from='idigbio', limit=20)
inspect(out)
} # }
```
