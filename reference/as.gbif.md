# Coerce occurrence keys to gbifkey/occkey objects

Coerce occurrence keys to gbifkey/occkey objects

## Usage

``` r
as.gbif(x, ...)
```

## Arguments

- x:

  Various inputs, including the output from a call to
  [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) (class
  occdat),
  [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md)
  (class data.frame), or a list, numeric, character, gbifkey, or occkey.

- ...:

  curl options; named parameters passed on to
  [`crul::HttpClient()`](https://docs.ropensci.org/crul/reference/HttpClient.html)

## Value

One or more in a list of both class gbifkey and occkey

## Details

Internally, we use
[`rgbif::occ_get()`](https://docs.ropensci.org/rgbif/reference/occ_get.html),
whereas [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) uses
[`rgbif::occ_data()`](https://docs.ropensci.org/rgbif/reference/occ_data.html).
We can use
[`rgbif::occ_get()`](https://docs.ropensci.org/rgbif/reference/occ_get.html)
here because we have the occurrence key to go directly to the occurrence
record.

## See also

Other coercion:
[`as.ala()`](https://docs.ropensci.org/spocc/reference/as.ala.md),
[`as.idigbio()`](https://docs.ropensci.org/spocc/reference/as.idigbio.md),
[`as.inat()`](https://docs.ropensci.org/spocc/reference/as.inat.md),
[`as.obis()`](https://docs.ropensci.org/spocc/reference/as.obis.md),
[`as.vertnet()`](https://docs.ropensci.org/spocc/reference/as.vertnet.md)

## Examples

``` r
if (FALSE) { # \dontrun{
spnames <- c('Accipiter striatus', 'Setophaga caerulescens', 
  'Spinus tristis')
out <- occ(query=spnames, from=c('gbif','ebird'), 
  gbifopts=list(hasCoordinate=TRUE), limit=2)
res <- occ2df(out)
(tt <- as.gbif(out))
(uu <- as.gbif(res))
as.gbif(as.numeric(res$key[1]))
as.gbif(res$key[1])
as.gbif(as.list(res$key[1:2]))
as.gbif(tt[[1]])
as.gbif(uu[[1]])
as.gbif(tt[1:2])
} # }
```
