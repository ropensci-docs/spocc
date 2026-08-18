# Coerce occurrence keys to vertnetkey/occkey objects

Coerce occurrence keys to vertnetkey/occkey objects

## Usage

``` r
as.vertnet(x)
```

## Arguments

- x:

  Various inputs, including the output from a call to
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) (class
  occdat),
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md)
  (class data.frame), or a list, numeric, character, vertnetkey, or
  occkey.

## Value

One or more in a list of both class vertnetkey and occkey

## Details

Internally, we use
[`rvertnet::vert_id()`](https://docs.ropensci.org/rvertnet/reference/vert_id.html),
whereas [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) uses
[`rvertnet::vertsearch()`](https://docs.ropensci.org/rvertnet/reference/vertsearch.html).

## See also

Other coercion:
[`as.ala()`](https://docs.ropensci.org/spocc/reference/as.ala.md),
[`as.gbif()`](https://docs.ropensci.org/spocc/reference/as.gbif.md),
[`as.idigbio()`](https://docs.ropensci.org/spocc/reference/as.idigbio.md),
[`as.inat()`](https://docs.ropensci.org/spocc/reference/as.inat.md),
[`as.obis()`](https://docs.ropensci.org/spocc/reference/as.obis.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# spnames <- c('Accipiter striatus', 'Setophaga caerulescens',
#   'Spinus tristis')
# out <- occ(query=spnames, from='vertnet', has_coords=TRUE, limit=2)
# res <- occ2df(out)
# (tt <- as.vertnet(out))
# (uu <- as.vertnet(res))
# keys <- Filter(Negate(is.na), res$key)
# as.vertnet(keys[1])
# as.vertnet(as.list(keys[1:2]))
# as.vertnet(tt[[1]])
# as.vertnet(uu[[1]])
# as.vertnet(tt[1:2])
} # }
```
