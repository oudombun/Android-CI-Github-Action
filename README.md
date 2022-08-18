Work flow :
1. push to master branch -> generate debug apk (debug.yml)
2. push to release/* branch -> generate release bundle (release.yml)
3. push to master branch -> upload release bundle to google play store (will update later)


*** Note ***

To create a release bundle, you have to perform the following steps:

-Create a release branch from master. This branch should follow the following naming convention: release/x.y.z where x.y.z is the target Android app version name.

-Bump both versionCode and versionName in app/build.gradle in the release branch.

-Create a pull request to merge release branch into master. The deploy Github Action will automatically execute against the release branch.