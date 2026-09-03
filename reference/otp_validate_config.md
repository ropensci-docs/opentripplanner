# Validate Config Object

Checks if the list of OTP configuration options is valid

## Usage

``` r
otp_validate_config(config, type = attributes(config)$config_type, version = 1)
```

## Arguments

- config:

  A named list made/modified from \`otp_make_config()\`

- type:

  type of config file

- version:

  version of OPT e.g. 1 or 2

## Details

Performs basic validity checks on class, max/min values etc as
appropriate, some of more complex parameters are not checked. For more
details see:

http://docs.opentripplanner.org/en/latest/Configuration
http://dev.opentripplanner.org/javadoc/1.3.0/org/opentripplanner/routing/core/RoutingRequest.html

## See also

Other setup:
[`otp_build_graph()`](https://docs.ropensci.org/opentripplanner/reference/otp_build_graph.md),
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_demo()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_demo.md),
[`otp_dl_jar()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_jar.md),
[`otp_make_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_config.md),
[`otp_setup()`](https://docs.ropensci.org/opentripplanner/reference/otp_setup.md),
[`otp_stop()`](https://docs.ropensci.org/opentripplanner/reference/otp_stop.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
conf <- otp_make_config("build")
otp_validate_config(conf)
} # }
```
