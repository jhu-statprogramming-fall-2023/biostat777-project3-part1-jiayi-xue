# jpeg

<!-- badges: start -->

<!-- badges: end -->

### URL to the GitHub link to the original R package:

<https://github.com/s-u/jpeg>

### URL to the deployed website that in Part 1E:

<https://jhu-statprogramming-fall-2023.github.io/biostat777-project3-part1-jiayi-xue/>

### 5 things customized in the pkgdown website (excluding adding the example data analysis from Part 1C):

1.  Change the bootswatch theme into 'minty'.

2.  The colours used for syntax highlighting in code blocks are changed into 'ayu-light' theme.

3.  Change the fonts of the text.

4.  Switch the position of the left and right navigation bar.

5.  Remove the homepage sidebar.

### Title: jpeg

### Author: Simon Urbanek

### Person who made the website and example data analysis: Jiayi Xue

### Goal:

The package can be used to read, write and display bitmap images stored in the JPEG format.

### Exported functions:

1.  readJPEG(): Read an image from a JPEG file/content into a raster array.
2.  writeJPEG(): Create a JPEG image from an array or matrix.

## Installation

You can install the development version of jpeg from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("s-u/jpeg")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r

library(jpeg)
## basic example code for readJPEG function:

# read a sample file (R logo)
    img <- readJPEG(system.file("img", "Rlogo.jpg", package="jpeg"))
    # read it also in native format
    img.n <- readJPEG(system.file("img", "Rlogo.jpg", package="jpeg"), TRUE)
    if (exists("rasterImage")) { # can plot only in R 2.11.0 and higher
      plot(1:2, type='n')
      rasterImage(img, 1.2, 1.27, 1.8, 1.73)
      rasterImage(img.n, 1.5, 1.5, 1.9, 1.8)
    }
    
```
