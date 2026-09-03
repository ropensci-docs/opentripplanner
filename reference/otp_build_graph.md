# Build an OTP Graph

OTP is run in Java and requires Java commands to be typed into the
command line. The function allows the parameters to be defined in R and
automatically passed to Java. This function builds a OTP graph from the
Open Street Map and other files.

## Usage

``` r
otp_build_graph(
  otp = NULL,
  dir = NULL,
  memory = 2048,
  router = "default",
  flag64bit = TRUE,
  quiet = TRUE,
  otp_version = NULL
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

  A character string for the name of the router, must subfolder of
  dir/graphs, default "default". See vignettes for details.

- flag64bit:

  Logical, if true the -d64 flag is added to Java instructions, ignored
  if otp_version \>= 2

- quiet:

  Logical, if FALSE the Java commands will be printed to console

- otp_version:

  Numeric, version of OTP to build, default NULL when version is
  auto-detected

## Value

Character vector of messages produced by OTP, and will return the
message "Graph built" if successful

## Details

The OTP .jar file can be downloaded from
https://repo1.maven.org/maven2/org/opentripplanner/otp/

To build an OTP graph requires the following files to be in the
directory specified by the dir variable.

/graphs - A sub-directory

/default - A sub-directory with the name of the OTP router used in
router' variable

osm.pbf - Required, pbf file containing the Open Street Map

router-config.json - Required, json file containing configurations
settings for the OTP

gtfs.zip - Optional, and number of GTFS files with transit timetables

terrain.tif - Optional, GeoTiff image of terrain map

The function will accept any file name for the .jar file, but it must be
the only .jar file in that directory OTP can support multiple routers
(e.g. different regions), each router must have its own sub-directory in
the graphs directory

## See also

Other setup:
[`otp_check_java()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_java.md),
[`otp_check_version()`](https://docs.ropensci.org/opentripplanner/reference/otp_check_version.md),
[`otp_dl_demo()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_demo.md),
[`otp_dl_jar()`](https://docs.ropensci.org/opentripplanner/reference/otp_dl_jar.md),
[`otp_make_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_make_config.md),
[`otp_setup()`](https://docs.ropensci.org/opentripplanner/reference/otp_setup.md),
[`otp_stop()`](https://docs.ropensci.org/opentripplanner/reference/otp_stop.md),
[`otp_validate_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_validate_config.md),
[`otp_write_config()`](https://docs.ropensci.org/opentripplanner/reference/otp_write_config.md)

## Examples

``` r
if (FALSE) { # \dontrun{
log <- otp_build_graph(otp = "C:/otp/otp.jar", dir = "C:/data")
} # }
```
