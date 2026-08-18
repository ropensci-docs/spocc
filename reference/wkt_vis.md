# Visualize well-known text area's on a map.

This can be helpful in visualizing the area in which you are searching
for occurrences with the
[`occ()`](https://docs.ropensci.org/spocc/reference/occ.md) function.

## Usage

``` r
wkt_vis(x, zoom = 6, maptype = "terrain", browse = TRUE)
```

## Arguments

- x:

  Input well-known text area (character)

- zoom:

  Zoom level, defaults to 6 (numeric)

- maptype:

  Map type, default is terrain (character)

- browse:

  Open in browser or not. If not, gives back path to html file. Default:
  `TRUE` (logical)

## Details

Uses Mapbox's map layers, openes in your default browser

## See also

Other bbox:
[`bbox2wkt()`](https://docs.ropensci.org/spocc/reference/bbox2wkt.md)

## Examples

``` r
if (FALSE) { # \dontrun{
poly <- 'POLYGON((-111.06 38.84, -110.80 39.37, -110.20 39.17, -110.20 38.90,
     -110.63 38.67, -111.06 38.84))'
wkt_vis(poly)

poly2 <- 'POLYGON((-125 38.4,-125 40.9,-121.8 40.9,-121.8 38.4,-125 38.4))'
wkt_vis(poly2)

# Multiple polygons
x <- "POLYGON((-125 38.4, -121.8 38.4, -121.8 40.9, -125 40.9, -125 38.4), 
(-115 22.4, -111.8 22.4, -111.8 30.9, -115 30.9, -115 22.4))"
wkt_vis(x)

# don't open in browser
poly2 <- 'POLYGON((-125 38.4,-125 40.9,-121.8 40.9,-121.8 38.4,-125 38.4))'
wkt_vis(poly2, browse = FALSE)
} # }
```
