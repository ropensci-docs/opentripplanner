# Write config object as json file

Takes a config list produced by \`otp_make_config()\` and saves it as
json file for OTP

## Usage

``` r
otp_write_config(config, dir = NULL, router = "default")
```

## Arguments

- config:

  A named list made/modified from \`otp_make_config()\`

- dir:

  Path to folder where data for OTP is to be stored

- router:

  name of the router, default is "default", must be a subfolder of
  dir/graphs

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
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
conf <- otp_make_config("build")
otp_write_config(conf, dir = tempdir())
} # }
```
