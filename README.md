# Maven parent POM for eXist Apps

This repository just contains the Maven parent artifact for eXist Apps.

It just contains a number of constant properties alongside fixed dependency and plugin versions.

## Install
If you wish to install this locally:
```bash
$ git clone https://github.com/exist-db/exist-apps-parent.git
$ cd exist-apps-parent
$ mvn clean install
```

## Release

Requirements: An install of GnuPG and a valid key for signing the release artifacts.

If you modify this POM and need to release a new version, make sure you have committed your changes and then run:

```bash
$ mvn release:prepare
$ mvn release:perform
$ git push
```

You can then visit http://oss.sonatype.org/ and login, to then publish the artifacts to Maven Central.
