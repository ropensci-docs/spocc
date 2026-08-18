# Coerce occurrence keys to iNaturalist id objects

Coerce occurrence keys to iNaturalist id objects

## Usage

``` r
as.inat(x, ...)
```

## Arguments

- x:

  Various inputs, including the output from a call to
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) (class
  occdat),
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md)
  (class data.frame), or a list, numeric, character, inatkey, or occkey.

- ...:

  curl options; named parameters passed on to
  [`crul::HttpClient()`](https://docs.ropensci.org/crul/reference/HttpClient.html)

## Value

One or more in a list of both class inatkey and occkey

## See also

Other coercion:
[`as.ala()`](https://docs.ropensci.org/spocc/reference/as.ala.md),
[`as.gbif()`](https://docs.ropensci.org/spocc/reference/as.gbif.md),
[`as.idigbio()`](https://docs.ropensci.org/spocc/reference/as.idigbio.md),
[`as.obis()`](https://docs.ropensci.org/spocc/reference/as.obis.md),
[`as.vertnet()`](https://docs.ropensci.org/spocc/reference/as.vertnet.md)

## Examples

``` r
if (FALSE) { # \dontrun{
spnames <- c('Accipiter striatus', 'Setophaga caerulescens',
  'Spinus tristis')
out <- occ(query=spnames, from='inat', limit=2)
res <- occ2df(out)
(tt <- as.inat(out))
(uu <- as.inat(res))
as.inat(res$key[1])
as.inat(as.list(res$key[1:2]))
as.inat(tt[[1]])
as.inat(uu[[1]])
as.inat(tt[1:2])
} # }
```
