# bstools-lib-template

This is a bare bones template intended to kick start creation of future `bstools` libraries.

## Required Information

Certain fields in the gradle configuration have been intentionally left blank for you to fill in based on your library's name, package structure and artifactory repo. The minimum information required is:

- `group` (`build.gradle`)
  - e.g. `com.lifeway.bsolutions.{kafka,mongo,etc.}`
- `archivesBaseName` (`build.gradle`)
  - The name of your lib (existing examples include `kafka-route` and `kafka-cache`)
- `uploadArchives.repositories.mavenDeployer.pom.artifactId` (`build.gradle`)
  - Typically the same as your `archivesBaseName`
- `uploadArchives.repositories.mavenDeployer.pom.groupId` (`build.gradle`)
  - Typically the same as your `group`, and should reference the destination of the artifact in artifactory
- `rootProject.name` (`settings.gradle`)
  - Typically the same as your `archivesBaseName`

The `dependencies` section of the `build.gradle` has also been left blank so you can add only the minimum dependencies your lib requires.