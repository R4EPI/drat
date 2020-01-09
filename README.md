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
