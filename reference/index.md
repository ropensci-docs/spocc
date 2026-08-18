# Package index

## General information

- [`spocc-package`](https://docs.ropensci.org/spocc/reference/spocc-package.md)
  : Interface to many species occurrence data sources

## Queries

- [`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) : Search
  for species occurrence data across many data sources.
- [`occ_names()`](https://docs.ropensci.org/spocc/reference/occ_names.md)
  : Search for species names across many data sources.
- [`occ_names_options()`](https://docs.ropensci.org/spocc/reference/occ_names_options.md)
  : Look up options for parameters passed to each source for occ_names
  function
- [`occ_options()`](https://docs.ropensci.org/spocc/reference/occ_options.md)
  : Look up options for parameters passed to each source
- [`print(`*`<occdat>`*`)`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)
  [`print(`*`<occdatind>`*`)`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)
  [`summary(`*`<occdat>`*`)`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)
  [`summary(`*`<occdatind>`*`)`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)
  [`print(`*`<occnames>`*`)`](https://docs.ropensci.org/spocc/reference/spocc_objects.md)
  : spocc objects and their print, plot, and summary methods

## Query helpers - Bounding boxes

- [`bbox2wkt()`](https://docs.ropensci.org/spocc/reference/bbox2wkt.md)
  [`wkt2bbox()`](https://docs.ropensci.org/spocc/reference/bbox2wkt.md)
  : Convert a bounding box to a Well Known Text polygon, and a WKT to a
  bounding box
- [`wkt_vis()`](https://docs.ropensci.org/spocc/reference/wkt_vis.md) :
  Visualize well-known text area's on a map.

## Output enrichment and cleaning

- [`inspect()`](https://docs.ropensci.org/spocc/reference/inspect.md) :
  Get more data on individual occurrences
- [`fixnames()`](https://docs.ropensci.org/spocc/reference/fixnames-defunct.md)
  : Change names to be the same for each taxon.
- [`spocc_duplicates`](https://docs.ropensci.org/spocc/reference/spocc_duplicates.md)
  : A note about duplicate occurrence records

## Output conversion

- [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md) :
  Combine results from occ calls to a single data.frame
- [`as.ala()`](https://docs.ropensci.org/spocc/reference/as.ala.md) :
  Coerce occurrence keys to ALA id objects
- [`as.gbif()`](https://docs.ropensci.org/spocc/reference/as.gbif.md) :
  Coerce occurrence keys to gbifkey/occkey objects
- [`as.idigbio()`](https://docs.ropensci.org/spocc/reference/as.idigbio.md)
  : Coerce occurrence keys to idigbio objects
- [`as.inat()`](https://docs.ropensci.org/spocc/reference/as.inat.md) :
  Coerce occurrence keys to iNaturalist id objects
- [`as.obis()`](https://docs.ropensci.org/spocc/reference/as.obis.md) :
  Coerce occurrence keys to obis id objects
- [`as.vertnet()`](https://docs.ropensci.org/spocc/reference/as.vertnet.md)
  : Coerce occurrence keys to vertnetkey/occkey objects
