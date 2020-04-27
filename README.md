
<!-- README.md is generated from README.Rmd. Please edit that file -->

![Build
packages](https://github.com/kvasilopoulos/drat/workflows/Build%20packages/badge.svg)

There are two ways to install packages from this [drat
repo](https://github.com/kvasilopoulos/drat).

1.  By specifying the repo in `install.packages()`

<!-- end list -->

``` r
install.packages('exuberdata', repos = 'https://kvasilopoulos.github.io/drat/', type = 'source')
```

2.  By registering `kvasilopoulos` repository as a valid repository

<!-- end list -->

``` r
install.packages("drat")
drat:::add("kvasilopoulos")
```

Now you can install and update packages without specfying the `repo` and
the `type`.

``` r
install.packages("exuberdata")
```

# Maintaining this page

## drat.builder and gh-actions

Instructions on the how to set up drat.builder with gh-actions are in
this [Post](https://zkamvar.netlify.app/) by [Zhian N.
Kamvar](https://github.com/zkamvar).

The packages included in this drat repository are maintained in the
[packages.txt](./packages.txt), which contains the github accounts and
names of the packages.

The data and metadata associated with this page are built with the
[{drat.builder}](https://github.com/richfitz/drat.builder) package.

## Automated builds

This page is maintained under a [GitHub
Action](https://github.com/kvasilopoulos/drat/actions?query=workflow%3A%22Build+packages%22)
that will check if the packages updated and build them to this repo. If
you want to update a package (e.g. change its version number), edit the
[packages.txt](./packages.txt) file and the [GitHub
Action](https://github.com/kvasilopoulos/drat/actions?query=workflow%3A%22Build+packages%22)
will update the packages automagically.

## Manual builds

Assuming the above works just fine, you shouldn’t have to use this, but
it is here for posterity.

Install {drat.builder} via {remotes}:

``` r
remotes::install_github("richfitz/drat.builder")
```

Steps for updating this page:

1.  Pull from the remote to make sure you have the entire history
2.  Open R from this directory
3.  Run `drat.builder::build()`
4.  push the changes

## Content

    #> [1] "exuberdata_0.0.0.9000.tar.gz" "exuberdata_0.0.0.9001.tar.gz"
    #> [3] "exuberdata_0.0.0.9003.tar.gz" "exuberdata_0.0.0.9004.tar.gz"
    #> [5] "exuberdata_0.0.0.9005.tar.gz" "exuberdata_0.0.0.9006.tar.gz"
    #> [7] "exuberdata_0.0.1.tar.gz"      "exuberdata_0.1.0.tar.gz"

## More

You can learn more about drat from the vignettes Drat for Package Users
and Drat for Package Authors.
