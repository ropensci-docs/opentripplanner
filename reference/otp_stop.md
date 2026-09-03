# Stop and OTP Instance

OTP is run in Java and requires Java commands to be typed into the
command line. The function allows the parameters to be defined in R and
automatically passed to Java. This function stops an already running OTP
instance

## Usage

``` r
otp_stop(warn = TRUE, kill_all = TRUE)
```

## Arguments

- warn:

  Logical, should you get a warning message

- kill_all:

  Logical, should all Java instances be killed?

## Value

This function return a message but no object

## Details

The function assumes you have run otp_setup()

## See also

Other setup:
[`otp_build_graph()`](https://docs.ropensci.org/opentripplanner/reference/otp_build_graph.md),
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_demo()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_demo.md),
[`otp_dl_jar()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_jar.md),
[`otp_make_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_config.md),
[`otp_setup()`](https://docs.ropensci.org/opentripplanner/reference/otp_setup.md),
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
otp_stop(kill_all = FALSE)
} # }
```
