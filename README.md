# Package Repository for the R4EPIs project

To install packages from the R4EPIs project, you should use the {drat} package:

```r
install.packages("drat", repos = "https://cran.rstudio.com")
```

Now you can use {drat} to register the R4EPIs repository as a valid repository:

```r
drat:::add("R4EPI")
```

Now you can install any of the R4Epis packages:

```r
install.packages("sitrep")
install.packages("apyramid")
install.packages("msfdict")
install.packages("epibuffet")
install.packages("msfmisc")
install.packages("linelist")   # RECON
install.packages("matchmaker") # RECON
```

# Maintaining this page

The packages included in this drat repository are maintained in the
[packages.txt], which contains the github accounts and names of
the packages.

The data and metadata associated with this page are built with the
[{drat.builder}](https://github.com/richfitz/drat.builder) package. 

## Automated builds

This page is maintained under a [GitHub Action] that will check if the packages
updated and build them to this repo. If you want to update a package (e.g.
change its version number), edit the [packages.txt] file and the [GitHub
Action] will update the packages automagically. 

## Manual builds

Assuming the above works just fine, you shouldn't have to use this, but it is
here for posterity.

Install {drat.builder} via {remotes}:

```r
remotes::install_github("richfitz/drat.builder")
```

Steps for updating this page:

1. Pull from the remote to make sure you have the entire history
2. Open R from this directory
3. Run `drat.builder::build()`
4. push the changes

[packages.txt]: ./packages.txt
[GitHub Action]: https://github.com/R4EPI/drat/actions?query=workflow%3A%22Build+packages%22
