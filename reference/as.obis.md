# Coerce occurrence keys to obis id objects

Coerce occurrence keys to obis id objects

## Usage

``` r
as.obis(x, ...)
```

## Arguments

- x:

  Various inputs, including the output from a call to
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) (class
  occdat),
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md)
  (class data.frame), or a list, numeric, obiskey, or occkey.

- ...:

  curl options; named parameters passed on to
  [`crul::HttpClient()`](https://docs.ropensci.org/crul/reference/HttpClient.html)

## Value

One or more in a list of both class obiskey and occkey

## See also

Other coercion:
[`as.ala()`](https://docs.ropensci.org/spocc/reference/as.ala.md),
[`as.gbif()`](https://docs.ropensci.org/spocc/reference/as.gbif.md),
[`as.idigbio()`](https://docs.ropensci.org/spocc/reference/as.idigbio.md),
[`as.inat()`](https://docs.ropensci.org/spocc/reference/as.inat.md),
[`as.vertnet()`](https://docs.ropensci.org/spocc/reference/as.vertnet.md)

## Examples

``` r
if (FALSE) { # \dontrun{
spnames <- c('Mola mola', 'Loligo vulgaris', 'Stomias boa')
out <- occ(query=spnames, from='obis', limit=2)
(res <- occ2df(out))
(tt <- as.obis(out))
(uu <- as.obis(res))
as.obis(x = res$key[1])
as.obis(as.list(res$key[1:2]))
as.obis(tt[[1]])
as.obis(uu[[1]])
as.obis(tt[1:2])

library("data.table")
rbindlist(lapply(tt, "[[", "results"),
  use.names = TRUE, fill = TRUE)
} # }
```
