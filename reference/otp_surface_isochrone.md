# Make an isochrone from a surface

Make a raster image (picture) of travel time using the surface features
in OTP 1.x

## Usage

``` r
otp_surface_isochrone(otpcon = NULL, surface = NULL)
```

## Arguments

- otpcon:

  OTP connection object produced by otp_connect()

- surface:

  A surface list from otp_make_surface()

## Value

Returns a data.frame of travel times

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
