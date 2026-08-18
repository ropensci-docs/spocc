# Coerce occurrence keys to idigbio objects

Coerce occurrence keys to idigbio objects

## Usage

``` r
as.idigbio(x, ...)
```

## Arguments

- x:

  Various inputs, including the output from a call to
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) (class
  occdat),
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md)
  (class data.frame), or a list, numeric, character, idigbiokey, or
  occkey.

- ...:

  curl options; named parameters passed on to
  [`httr::GET()`](https://httr.r-lib.org/reference/GET.html)

## Value

One or more in a list of both class idigbiokey and occkey

## Details

Internally, we use
[`idig_view_records`](https://idigbio.github.io/ridigbio/reference/idig_view_records.html),
whereas we use
[`idig_search_records`](https://idigbio.github.io/ridigbio/reference/idig_search_records.html)
in the [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md)
function.

## See also

Other coercion:
[`as.ala()`](https://docs.ropensci.org/spocc/reference/as.ala.md),
[`as.gbif()`](https://docs.ropensci.org/spocc/reference/as.gbif.md),
[`as.inat()`](https://docs.ropensci.org/spocc/reference/as.inat.md),
[`as.obis()`](https://docs.ropensci.org/spocc/reference/as.obis.md),
[`as.vertnet()`](https://docs.ropensci.org/spocc/reference/as.vertnet.md)

## Examples

``` r
if (FALSE) { # \dontrun{
spnames <- c('Accipiter striatus', 'Setophaga caerulescens',
  'Spinus tristis')
out <- occ(query=spnames, from='idigbio', limit=2)
res <- occ2df(out)
(tt <- as.idigbio(out))
(uu <- as.idigbio(res))
as.idigbio(res$key[1])
as.idigbio(as.list(res$key[1:2]))
as.idigbio(tt[[1]])
as.idigbio(uu[[1]])
as.idigbio(tt[1:2])

library("dplyr")
bind_rows(lapply(tt, function(x) data.frame(unclass(x)$data)))
} # }
```
