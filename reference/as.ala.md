# Coerce occurrence keys to ALA id objects

Coerce occurrence keys to ALA id objects

## Usage

``` r
as.ala(x, ...)
```

## Arguments

- x:

  Various inputs, including the output from a call to
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) (class
  occdat),
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md)
  (class data.frame), or a list, numeric, alakey, or occkey.

- ...:

  curl options; named parameters passed on to
  [`crul::HttpClient()`](https://docs.ropensci.org/crul/reference/HttpClient.html)

## Value

One or more in a list of both class alakey and occkey

## See also

Other coercion:
[`as.gbif()`](https://docs.ropensci.org/spocc/reference/as.gbif.md),
[`as.idigbio()`](https://docs.ropensci.org/spocc/reference/as.idigbio.md),
[`as.inat()`](https://docs.ropensci.org/spocc/reference/as.inat.md),
[`as.obis()`](https://docs.ropensci.org/spocc/reference/as.obis.md),
[`as.vertnet()`](https://docs.ropensci.org/spocc/reference/as.vertnet.md)

## Examples

``` r
if (FALSE) { # \dontrun{
spnames <- c('Barnardius zonarius', 'Grus rubicunda', 'Cracticus tibicen')
out <- occ(query=spnames, from='ala', limit=2)
(res <- occ2df(out))
(tt <- as.ala(out))
as.ala(x = res$key[1])
} # }
```
