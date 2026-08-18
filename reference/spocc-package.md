# Interface to many species occurrence data sources

A programmatic interface to many species occurrence data sources,
including GBIF, iNaturalist, Berkeley Ecoinformatics Engine, eBird,
iDigBio, VertNet, OBIS, and ALA. Includes functionality for retrieving
species occurrence data, and combining that data.

## Package API

The main function to use is
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) - a single
interface to many species occurrence databases (see below for a list).

Other functions include:

- [`occ2df()`](https://docs.ropensci.org/spocc/reference/occ2df.md) -
  Combine results from `occ` into a data.frame

- [`wkt_vis()`](https://docs.ropensci.org/spocc/reference/wkt_vis.md) -
  Visualize WKT strings (used to define geometry based searches for some
  data sources) in an interactive map

## Currently supported species occurrence data sources

|             |                                   |
|-------------|-----------------------------------|
| Provider    | Web                               |
| GBIF        | <https://www.gbif.org/>           |
| eBird       | <http://ebird.org/content/ebird/> |
| iNaturalist | <https://www.inaturalist.org/>    |
| VertNet     | <http://vertnet.org/>             |
| iDigBio     | <https://www.idigbio.org/>        |
| OBIS        | <https://www.obis.org/>           |
| ALA         | <https://www.ala.org.au/>         |

## Duplicates

See
[`spocc_duplicates()`](https://docs.ropensci.org/spocc/reference/spocc_duplicates.md)
for more.

## Clean data

All data cleaning functionality is in as archived package: `scrubr`
(<https://github.com/ropensci-archive/scrubr>). On CRAN:
<https://cran.r-project.org/src/contrib/Archive/scrubr/>. See also
package <https://cran.r-project.org/package=CoordinateCleaner>

## Make maps

All mapping functionality is now in a separate package:
``` mapr`` (<https://github.com/ropensci/mapr>) (formerly known as  ```spoccutils\`).
On CRAN: <https://cran.r-project.org/package=mapr>

## Author

Scott Chamberlain
