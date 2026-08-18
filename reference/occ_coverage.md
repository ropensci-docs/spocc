# Automatically generate coverages for a spocc search

This function will automatically generate metadata for spocc queries
that can then be converted to other standards.

## Usage

``` r
occ_coverage(occObj, coverage = "all")
```

## Arguments

- occObj:

  an search object returned by occ

- coverage:

  a vector of coverage types to generate. These include
  'temporal','spatial','taxa', or just 'all'.
