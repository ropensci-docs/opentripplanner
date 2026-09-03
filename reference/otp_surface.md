# Evaluate a surface against a pointset

Evaluate a surface created with \`otp_make_surface\` against a pointset
made with \`otp_pointset\` to get travel times and statitics from the
analysit in OTP 1.x

## Usage

``` r
otp_surface(
  otpcon = NULL,
  surface = NULL,
  pointsset = NULL,
  get_data = TRUE,
  ncores = 1
)
```

## Arguments

- otpcon:

  OTP connection object produced by otp_connect()

- surface:

  A surface list from otp_make_surface()

- pointsset:

  character, name of pointset

- get_data:

  Logical, should data be returned or just travel times.

- ncores:

  Integer, number of cores to use

## Value

Returns a list of data.frames of travel times

## Details

THis function requires the analysis and pointset features to be enabled
during \`otp_setup()\`. Thus it will only work with OTP 1.x. For more
detail see the analyst vignette.

## Examples

``` r
if (FALSE) { # \dontrun{
times <- otp_surface(otpcon, c(-1.17502, 50.64590), "lsoa", path_data)
} # }
```
