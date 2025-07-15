# Maven parent POM for EXPath Packages in eXist-db

[![Build Status](https://github.com/eXist-db/exist-apps-parent/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/eXist-db/exist-apps-parent/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/license-LGPL%202.1%20only-blue.svg)](https://www.gnu.org/licenses/lgpl-2.1.html)
[![Maven Central](https://img.shields.io/maven-central/v/org.exist-db/exist-apps-parent?label=maven+central)](https://central.sonatype.com/search?namespace=org.exist-db)

This repository contains a Maven parent POM that you may use as the basis of your EXPath Packages for eXist-db.
It defines a number of sensible defaults and versions that can help you get started quickly in your own projects.

It just contains a number of constant properties alongside fixed dependency and plugin versions.

## Using
If you would like to use this as a base for your own EXPath Package, then you can add the following to the top of your package's `pom.xml` file:

```xml
    <parent>
        <groupId>org.exist-db</groupId>
        <artifactId>exist-apps-parent</artifactId>
        <version>1.12.0</version>
        <relativePath/>
    </parent>
```

If you are looking for a quick way to generate a skeleton for your EXPath Package, you should take a look at the: [[exist-apps-archetype](https://github.com/exist-db/exist-apps-archetype).

## Install
If you wish to install this locally:

```bash
$ git clone https://github.com/exist-db/exist-apps-parent.git
$ cd exist-apps-parent
$ ./mvnw clean install
```

NOTE: If you are on a Windows platform, you should replace `./mvnw` above with `mvn`.

## Release

Requirements: An install of GnuPG and a valid key for signing the release artifacts.

If you modify this POM and need to release a new version, make sure you have committed your changes and then run:

```bash
$ ./mvnw release:prepare
$ ./mvnw release:perform
$ git push
```

NOTE: If you are on a Windows platform, you should replace `./mvnw` above with `mvn`.

You can then visit https://central.sonatype.com/ and login, to then publish the artifacts to Maven Central.
