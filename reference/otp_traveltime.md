# Get travel times between points

This function requires OTP 1.x and the analyst

## Usage

``` r
otp_traveltime(
  otpcon = NA,
  path_data = NULL,
  fromPlace = NA,
  toPlace = NA,
  fromID = NULL,
  toID = NULL,
  mode = "CAR",
  date_time = Sys.time(),
  arriveBy = FALSE,
  maxWalkDistance = 1000,
  numItineraries = 3,
  routeOptions = NULL,
  ncores = max(round(parallel::detectCores() * 1.25) - 1, 1),
  timezone = otpcon$timezone
)
```

## Arguments

- otpcon:

  OTP connection object produced by otp_connect()

- path_data:

  Path to data used in otp_build_graph()

- fromPlace:

  Numeric vector, Longitude/Latitude pair, e.g.
  \`c(-0.134649,51.529258)\`, or 2 column matrix of Longitude/Latitude
  pairs, or sf data frame of POINTS with CRS 4326

- toPlace:

  Numeric vector, Longitude/Latitude pair, e.g.
  \`c(-0.088780,51.506383)\`, or 2 column matrix of Longitude/Latitude
  pairs, or sf data frame of POINTS with CRS 4326

- fromID:

  character vector same length as fromPlace

- toID:

  character vector same length as toPlace

- mode:

  character vector of one or more modes of travel valid values TRANSIT,
  WALK, BICYCLE, CAR, BUS, RAIL, default CAR. Not all combinations are
  valid e.g. c("WALK","BUS") is valid but c("WALK","CAR") is not.

- date_time:

  POSIXct, a date and time, defaults to current date and time

- arriveBy:

  Logical, Whether the trip should depart or arrive at the specified
  date and time, default FALSE

- maxWalkDistance:

  Numeric passed to OTP in metres

- numItineraries:

  The maximum number of possible itineraries to return

- routeOptions:

  Named list of values passed to OTP use \`otp_route_options()\` to make
  template object.

- ncores:

  Numeric, number of cores to use when batch processing, default 1, see
  details

- timezone:

  Character, what timezone to use, see as.POSIXct, default is local
  timezone

## Value

Returns an data frame

## Details

Make a travel time matrix using the analyst features in OPT 1.x

## See also

Other analyst:
[`otp_make_surface()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_surface.md)
