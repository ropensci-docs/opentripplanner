# Download Demo Data

Download the demonstration data for the Isle of Wight

## Usage

``` r
otp_dl_demo(
  path_data = NULL,
  url = paste0("https://github.com/ropensci/opentripplanner/",
    "releases/download/0.1/isle-of-wight-demo.zip"),
  quiet = FALSE
)
```

## Arguments

- path_data:

  path to folder where data for OTP is to be stored

- url:

  URL to data

- quiet:

  logical, passed to download.file, default FALSE

## See also

Other setup:
[`otp_build_graph()`](https://docs.ropensci.org/opentripplanner/reference/otp_build_graph.md),
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_jar()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_jar.md),
[`otp_make_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_config.md),
[`otp_setup()`](https://docs.ropensci.org/opentripplanner/reference/otp_setup.md),
[`otp_stop()`](https://docs.ropensci.org/opentripplanner/reference/otp_stop.md),
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
otp_dl_demo(tempdir())
} # }
```
