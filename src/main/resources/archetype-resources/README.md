# ${rPackageName}

[![R-CMD-check](https://github.com/${githubOrganisation}/${githubRepository}/workflows/R-CMD-check/badge.svg)](https://github.com/${githubOrganisation}/${githubRepository}/actions)

This template readme should be updated to include documentation for the end users of your R-package. The following links will take you to the R library documentation (e.g. pkgdown site) once this has been generated from the Java code, and assuming Github pages has been enabled for the repository.  

see the [full docs](https://${githubOrganisation}.github.io/${rPackageName})

see the [r package](https://${githubOrganisation}.github.io/${rPackageName}/docs/)

see the [javadoc](https://${githubOrganisation}.github.io/${rPackageName}/docs/javadoc/)

## Development notes

To generate the R code from the Java classes in this example library run: 

```BASH
cd ~/Git/${githubRepository}/src
mvn install
```
Then to use it in R:

```R
library(devtools)
# assuming you have cloned this repository locally:
load_all("~/Git/${githubRepository}")

# install_github("${githubOrganisation}/${githubRepository}")

# a basic smoke test
J <- ${rPackageName}::JavaApi$get()

# exploring the API using autocomplete in RStudio
# is a matter of typing J$<ctrl-space> 

tmp = J$BasicExample$new()
tmp$doHelloWorld()

# generated documentation available

?${rPackageName}-package
?${rPackageName}::BasicExample

```


