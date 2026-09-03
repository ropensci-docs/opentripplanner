# Use OTP Geo-coder to find a location

Geo-coding converts a named place, such as a street name into a lng/lat
pair.

## Usage

``` r
otp_geocode(
  otpcon = NULL,
  query = NULL,
  autocomplete = FALSE,
  stops = TRUE,
  clusters = FALSE,
  corners = TRUE,
  type = "SF"
)
```

## Arguments

- otpcon:

  OTP connection object produced by otp_connect()

- query:

  Character, The query string we want to geocode

- autocomplete:

  logical Whether we should use the query string to do a prefix match,
  default FALSE

- stops:

  Logical, Search for stops, either by name or stop code, default TRUE

- clusters:

  Logical, Search for clusters by their name, default FALSE

- corners:

  Logical, Search for street corners using at least one of the street
  names, default TRUE

- type:

  Character, How should results be returned can be "SF" or "Coordinates"
  or "Both", Default "SF"

## Value

Returns a data.frame of SF POINTS or Coordinates of all the locations
that match \`query\`

## Details

OTP will return a maximum of 10 results

## See also

Other routing:
[`otp_isochrone()`](https://docs.ropensci.org/opentripplanner/reference/otp_isochrone.md),
[`otp_plan()`](https://docs.ropensci.org/opentripplanner/reference/otp_plan.md),
[`otp_pointset()`](https://docs.ropensci.org/opentripplanner/reference/otp_pointset.md),
[`otp_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_routing_options.md),
[`otp_validate_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_routing_options.md)

## Examples

``` r
if (FALSE) { # \dontrun{
locations <- otp_geocode(otpcon, "High Street")
} # }
```
