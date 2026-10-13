# OBIS search

OBIS search

## Usage

``` r
obis_search(
  scientificName = NULL,
  size = 500,
  after = NULL,
  taxonid = NULL,
  aphiaid = NULL,
  areaid = NULL,
  datasetid = NULL,
  instituteid = NULL,
  nodeid = NULL,
  startdate = NULL,
  enddate = NULL,
  startdepth = NULL,
  enddepth = NULL,
  geometry = NULL,
  exclude = NULL,
  fields = NULL,
  ...
)
```

## Arguments

- scientificName:

  (character) Scientific name. Leave empty to include all taxa. This is
  what we pass your name query to

- size:

  (integer) number of results to fetch

- after:

  (character) Occurrence UUID up to which to skip.

- taxonid:

  (character) Taxon AphiaID.

- areaid:

  (character) Area ID.

- datasetid:

  (character) Dataset UUID.

- instituteid:

  (character) Institute ID.

- nodeid:

  (character) Node UUID.

- startdate:

  (character) Start date formatted as YYYY-MM-DD.

- enddate:

  (character) End date formatted as YYYY-MM-DD.

- startdepth:

  (integer) Start depth, in meters.

- enddepth:

  (integer) End depth, in meters.

- geometry:

  (character) Geometry, formatted as WKT.

- exclude:

  (character) set of quality flags to be excluded. one or more in a
  vector

- fields:

  (character) Field to be included in the result set. one or more in a
  vector
