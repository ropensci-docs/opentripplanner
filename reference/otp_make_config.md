# Make Config Object

OTP can be configured using three json files \`otp-config.json\`,
\`build-config.json\`, and \`router-config.json\`. This function creates
a named list for each config file and populates the defaults values.

## Usage

``` r
otp_make_config(type, version = 1)
```

## Arguments

- type:

  Which type of config file to create, "otp", "build", "router"

- version:

  version of OPT e.g. 1 or 2

## Details

For more details see:
http://docs.opentripplanner.org/en/latest/Configuration

## See also

Other setup:
[`otp_build_graph()`](https://docs.ropensci.org/opentripplanner/reference/otp_build_graph.md),
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_demo()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_demo.md),
[`otp_dl_jar()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_jar.md),
[`otp_setup()`](https://docs.ropensci.org/opentripplanner/reference/otp_setup.md),
[`otp_stop()`](https://docs.ropensci.org/opentripplanner/reference/otp_stop.md),
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
{
  conf <- otp_make_config("build")
  conf <- otp_make_config("router")
}
```
