# Set up an OTP instance.

OTP is run in Java and requires Java commands to be typed into the
command line. The function allows the parameters to be defined in R and
automatically passed to Java. This function sets up a local instance of
OTP, for remote versions see documentation.

The function assumes you have run otp_build_graph()

## Usage

``` r
otp_setup(
  otp = NULL,
  dir = NULL,
  memory = 2048,
  router = "default",
  port = 8080,
  securePort = 8081,
  analyst = FALSE,
  pointsets = FALSE,
  wait = TRUE,
  flag64bit = TRUE,
  quiet = TRUE,
  otp_version = NULL,
  open_browser = TRUE
)
```

## Arguments

- otp:

  A character string, path to the OTP .jar file

- dir:

  A character string, path to a directory containing the necessary
  files, see details

- memory:

  A positive integer. Amount of memory to assign to the OTP in MB,
  default is 2048

- router:

  A character for the name of the router to use, must be subfolder of
  dir/graphs, default "default". See vignettes for details.

- port:

  A positive integer. Optional, default is 8080.

- securePort:

  A positive integer. Optional, default is 8081.

- analyst:

  Logical. Should the analyst features be loaded? Default FALSE

- pointsets:

  Logical. Should the pointsets be loaded? Default FALSE

- wait:

  Logical, Should R wait until OTP has loaded before running next line
  of code, default TRUE

- flag64bit:

  Logical, if true the -d64 flag is added to Java instructions, ignored
  if otp_version \>= 2

- quiet:

  Logical, if FALSE the Java commands will be printed to console

- otp_version:

  Numeric, version of OTP to build, default NULL when version is
  auto-detected

- open_browser:

  Logical, if TRUE web browser is loaded when OTP is ready

## Value

This function does not return a value to R. If wait is TRUE R will wait
until OTP is running (maximum of 5 minutes). After 5 minutes (or if wait
is FALSE) the function will return R to your control, but the OTP will
keep loading.

## Details

To run an OTP graph must have been created using otp_build_graph and the
following files to be in the directory specified by the dir variable.

/graphs - A sub-directory

/default - A sub-directory with the name of the OTP router used in
'router' variable

graph.obj OTP graph

## See also

Other setup:
[`otp_build_graph()`](https://docs.ropensci.org/opentripplanner/reference/otp_build_graph.md),
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_demo()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_demo.md),
[`otp_dl_jar()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_jar.md),
[`otp_make_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_config.md),
[`otp_stop()`](https://docs.ropensci.org/opentripplanner/reference/otp_stop.md),
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
otp_setup(
  otp = "C:/otp/otp.jar",
  dir = "C:/data"
)
otp_setup(
  otp = "C:/otp/otp.jar",
  dir = "C:/data",
  memory = 5000,
  analyst = TRUE
)
} # }
```
