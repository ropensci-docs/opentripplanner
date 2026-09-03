# Make routingOptions object

OTP supports a wide selection of routing options \`otp_plan()\` accepts
a named list of these options. This function produces an empty named
list of valid options supported by both this package and OTP.

## Usage

``` r
otp_routing_options()
```

## Details

Supports almost all of the possible options in OTP 1.4. Note that some
of the most popular option (mode, date, time, etc.) are set directly in
\`otp_plan()\`. If you want to permenaty set an option many are
supported in the config files, see help on \`otp_make_config()\`.

http://dev.opentripplanner.org/apidoc/1.4.0/resource_PlannerResource.html

## See also

Other routing:
[`otp_geocode()`](https://docs.ropensci.org/opentripplanner/reference/otp_geocode.md),
[`otp_isochrone()`](https://docs.ropensci.org/opentripplanner/reference/otp_isochrone.md),
[`otp_plan()`](https://docs.ropensci.org/opentripplanner/reference/otp_plan.md),
[`otp_pointset()`](https://docs.ropensci.org/opentripplanner/reference/otp_pointset.md),
[`otp_validate_routing_options()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_routing_options.md)

## Examples

``` r
if (FALSE) { # \dontrun{
routingOptions <- otp_routing_options()
routingOptions$walkSpeed <- 1.5
routingOptions <- otp_validate_routing_options(routingOptions)
} # }
```
