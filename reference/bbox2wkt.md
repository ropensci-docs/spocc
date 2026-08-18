# Convert a bounding box to a Well Known Text polygon, and a WKT to a bounding box

Convert a bounding box to a Well Known Text polygon, and a WKT to a
bounding box

## Usage

``` r
bbox2wkt(minx = NA, miny = NA, maxx = NA, maxy = NA, bbox = NULL)

wkt2bbox(wkt)
```

## Arguments

- minx:

  Minimum x value, or the most western longitude

- miny:

  Minimum y value, or the most southern latitude

- maxx:

  Maximum x value, or the most eastern longitude

- maxy:

  Maximum y value, or the most northern latitude

- bbox:

  A vector of length 4, with the elements: minx, miny, maxx, maxy

- wkt:

  A Well Known Text string

## Value

bbox2wkt returns an object of class charactere, a Well Known Text string
of the form 'POLYGON((minx miny, maxx miny, maxx maxy, minx maxy, minx
miny))'

wkt2bbox returns a numeric vector of length 4, like c(minx, miny, maxx,
maxy).

## See also

Other bbox:
[`wkt_vis()`](https://docs.ropensci.org/spocc/reference/wkt_vis.md)

Other bbox:
[`wkt_vis()`](https://docs.ropensci.org/spocc/reference/wkt_vis.md)

## Examples

``` r
# Convert a bounding box to a WKT

## Pass in a vector of length 4 with all values
bbox2wkt(bbox = c(-125.0,38.4,-121.8,40.9))
#> [1] "POLYGON((-125 38.4,-121.8 38.4,-121.8 40.9,-125 40.9,-125 38.4))"

## Or pass in each value separately
bbox2wkt(-125.0, 38.4, -121.8, 40.9)
#> [1] "POLYGON((-125 38.4,-121.8 38.4,-121.8 40.9,-125 40.9,-125 38.4))"

# Convert a WKT object to a bounding box
wkt <- "POLYGON((-125 38.4,-125 40.9,-121.8 40.9,-121.8 38.4,-125 38.4))"
wkt2bbox(wkt)
#>   xmin ymin   xmax ymax
#> 1 -125 38.4 -121.8 40.9

identical(
 bbox2wkt(-125.0, 38.4, -121.8, 40.9),
 "POLYGON((-125 38.4,-121.8 38.4,-121.8 40.9,-125 40.9,-125 38.4))"
)
#> [1] TRUE

identical(
 c(-125.0, 38.4, -121.8, 40.9),
 as.numeric(
   wkt2bbox(
     "POLYGON((-125 38.4,-125 40.9,-121.8 40.9,-121.8 38.4,-125 38.4))"
   )
 )
)
#> [1] TRUE
```
