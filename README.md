# r6-generator-maven-archetype

Archetype to setup r6-generator maven projects for R to Java library integration.

The archetype needs the following information:

* githubOrganisation
* githubRepository
* rPackageName - optional, defaults to githubRepository name
* versionId - optional, defaults to main-SNAPSHOT
* rPackageVersion - optional, defaults to 0.0.0.9000
* rPackageLicense - optional, defaults to MIT
* maintainerName - optional, defaults to an example name
* maintainerSurname
* maintainerEmail
* maintainerOrganisation - optional, defaults to same as githubOrganisation.

Usage

```BASH
cd ~/Git
mvn archetype:generate \
  -DarchetypeGroupId=com.github.terminological \
  -DarchetypeArtifactId=r6-generator-maven-archetype \
  -DarchetypeVersion=master-SNAPSHOT \
  -DgithubOrganisation=exampleOrganisation \
  -DgithubRepository=examplePackage
``` 

The newly created Java project will be in the examplePackage subdirectory.

To generate the R package from the Java project it needs to be installed.


```BASH
cd ~/Git/examplePackage
mvn install
```
