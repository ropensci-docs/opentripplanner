# Get the Isochrones from a location

Get the Isochrones from a location

## Usage

``` r
otp_isochrone(
  otpcon = NA,
  fromPlace = NA,
  fromID = NULL,
  mode = "CAR",
  date_time = Sys.time(),
  arriveBy = FALSE,
  maxWalkDistance = 1000,
  routingOptions = NULL,
  cutoffSec = c(600, 1200, 1800, 2400, 3000, 3600),
  ncores = max(round(parallel::detectCores() * 1.25) - 1, 1),
  timezone = otpcon$timezone
)
```

## Arguments

- otpcon:

  OTP connection object produced by otp_connect()

- fromPlace:

  Numeric vector, Longitude/Latitude pair, e.g.
  \`c(-0.134649,51.529258)\`, or 2 column matrix of Longitude/Latitude
  pairs, or sf data frame of POINTS

- fromID:

  character vector same length as fromPlace

- mode:

  character vector of one or more modes of travel valid values
  "TRANSIT","BUS", "RAIL", "SUBWAY","TRAM", "FERRY", "GONDOLA",
  "FUNICULAR", "AIRPLANE", "CABLE_CAR", "WALK", "BICYCLE",
  "BICYCLE_RENT", "BICYCLE_PARK", "CAR", "CAR_PARK", "CAR_HAIL",
  "CARPOOL", "CAR_DROPOFF", "CAR_PICKUP", default CAR. Not all
  combinations are valid e.g. c("WALK","BUS") is valid but
  c("WALK","CAR") is not.

- date_time:

  POSIXct, a date and time, defaults to current date and time

- arriveBy:

  Logical, Whether the trip should depart or arrive at the specified
  date and time, default FALSE

- maxWalkDistance:

  maximum distance to walk in metres

- routingOptions:

  named list passed to OTP see \`otp_routing_options()\`

- cutoffSec:

  Numeric vector, number of seconds to define the break points of each
  Isochrone

- ncores:

  number of cores to use in parallel processing

- timezone:

  character, timezone to use, default from otpcon

## Value

Returns a SF data.frame of POLYGONs

## Details

Isochrones are maps of equal travel time, for a given location a map is
produced showing how long it takes to reach each location.

Isochrones are only available from OTP v1.x and will not work with v2.0

## See also

Other routing:
[`otp_geocode()`](https://docs.ropensci.org/opentripplanner/reference/otp_geocode.md),
[`otp_plan()`](https://docs.ropensci.org/opentripplanner/reference/otp_plan.md),
[`otp_pointset()`](https://docs.ropensci.org/opentripplanner/reference/otp_pointset.md),
[`otp_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_routing_options.md),
[`otp_validate_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_routing_options.md)

## Examples

``` r
if (FALSE) { # \dontrun{
isochrone1 <- otp_isochrone(otpcon, fromPlace = c(-0.1346, 51.5292))
isochrone2 <- otp_isochrone(otpcon,
  fromPlace = c(-0.1346, 51.5292),
  mode = c("WALK", "TRANSIT"), cutoffSec = c(600, 1200, 1800)
)
} # }
```
