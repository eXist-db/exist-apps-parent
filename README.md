# Maven parent POM for eXist Apps

This repository just contains the Maven parent artifact for eXist Apps.

It just contains a number of constant properties alongside fixed dependency and plugin versions.

## Use
If you wish to use this as a base for your eXist EXPath App, then you can add the following to your `pom.xml`:

```xml
    <parent>
        <groupId>org.exist-db</groupId>
        <artifactId>exist-apps-parent</artifactId>
        <version>1.12.0</version>
        <relativePath/>
    </parent>
```

If you are just starting out with creating an eXist EXPath App, then you may be interested to use [exist-apps-archetype](https://github.com/exist-db/exist-apps-archetype) which will create a skeleton app for your.

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
