# Create a pointset

Pointsets are text files tha can be used by the Analyist feature in OTP
1.5

## Usage

``` r
otp_pointset(points = NULL, name = NULL, dir = NULL)
```

## Arguments

- points:

  sf data frame of POINTS with CRS 4326

- name:

  Character, name for pointset

- dir:

  A character string, path to a directory containing the necessary
  files, see details

## Value

Returns a data.frame of SF POINTS or Coordinates of all the locations
that match \`query\`

## Details

OTP will return a maximum of 10 results

## See also

Other routing:
[`otp_geocode()`](https://docs.ropensci.org/opentripplanner/reference/otp_geocode.md),
[`otp_isochrone()`](https://docs.ropensci.org/opentripplanner/reference/otp_isochrone.md),
[`otp_plan()`](https://docs.ropensci.org/opentripplanner/reference/otp_plan.md),
[`otp_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_routing_options.md),
[`otp_validate_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_routing_options.md)

## Examples

``` r
if (FALSE) { # \dontrun{
locations <- otp_geocode(otpcon, "High Street")
} # }
```
