# Download OTP Jar File

Download the OTP jar file from maven.org

## Usage

``` r
otp_dl_jar(
  path = NULL,
  version = "1.5.0",
  file_name = paste0("otp-", version, "-shaded.jar"),
  url = "https://repo1.maven.org/maven2/org/opentripplanner/otp",
  quiet = FALSE,
  cache = TRUE
)
```

## Arguments

- path:

  path to folder where OTP is to be stored

- version:

  a character string of the version number default is "1.5.0"

- file_name:

  file name to give the otp default "otp.jar"

- url:

  URL to the download server

- quiet:

  logical, passed to download.file, default FALSE

- cache:

  logical, default TRUE, see details

## Value

The path to the OTP file

## Details

As of version 0.3.0.0 \`otp_dl_jar\` will cache the JAR file within the
package and ignore the \`path\` argument. You can force a new download
to be saved in the \`path\` location by setting \`cache = FALSE\`.

## See also

Other setup:
[`otp_build_graph()`](https://docs.ropensci.org/opentripplanner/reference/otp_build_graph.md),
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_demo()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_demo.md),
[`otp_make_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_config.md),
[`otp_setup()`](https://docs.ropensci.org/opentripplanner/reference/otp_setup.md),
[`otp_stop()`](https://docs.ropensci.org/opentripplanner/reference/otp_stop.md),
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
otp_dl_jar(tempdir())
} # }
```
