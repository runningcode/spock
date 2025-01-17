[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/spockframework/spock/blob/master/LICENSE)
[![Maven Central](https://img.shields.io/maven-central/v/org.spockframework/spock-core.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:org.spockframework)
[![Build](https://img.shields.io/github/checks-status/spockframework/spock/master?label=Build)](https://github.com/spockframework/spock/actions?query=workflow%3A%22CI+Builds%22+branch%3Amaster)
[![Jitpack](https://jitpack.io/v/org.spockframework/spock.svg)](https://jitpack.io/#org.spockframework/spock)
[![Codecov](https://codecov.io/gh/spockframework/spock/branch/master/graph/badge.svg)](https://codecov.io/gh/spockframework/spock)
[![Gitter](https://badges.gitter.im/spockframework/spock.svg)](https://gitter.im/spockframework/spock?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![Revved up by Gradle Enterprise](https://img.shields.io/badge/Revved%20up%20by-Gradle%20Enterprise-06A0CE?logo=Gradle&labelColor=02303A)](https://ge.spockframework.org/scans)


Spock Framework
===============

Spock is a BDD-style developer testing and specification framework for Java and [Groovy](https://groovy-lang.org/) applications.
To learn more about Spock, visit http://spockframework.org. To run a sample spec in your browser, go to
http://webconsole.spockframework.org.

Latest Versions
---------------
* The latest 1.x release version is **1.3** (1.3-groovy-2.4, 1.3-groovy-2.5), released on 2019-01-22.
* The latest 2.0 release version is **2.0-M5** (2.0-M5-groovy-2.5, 2.0-M5-groovy-3.0), released on 2021-03-23.
* The current development version is **2.0-SNAPSHOT** (2.0-groovy-2.5-SNAPSHOT, 2.0-groovy-3.0-SNAPSHOT).

**NOTE:** Spock 1.3 is the last release for 1.x based on JUnit 4. Spock 2.0 is based on the JUnit 5 Platform
          and require Java 8/groovy-2.5

Releases are available from [Maven Central](https://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.spockframework%22).
Development snapshots are available from [Sonatype OSS](https://oss.sonatype.org/content/repositories/snapshots/org/spockframework/).

### Ad-Hoc Intermediate Releases

For intermediate stable builds we recommend to use [Jitpack](https://jitpack.io/#org.spockframework/spock) (go here for instructions):

1. Add https://jitpack.io as a repository
2. Use `org.spockframework.spock` as `groupId` and the normal `artifact-id`

```groovy
repositories {
    // ...
    maven { url 'https://jitpack.io' }
}

dependencies {
        compile 'org.spockframework.spock:spock-core:spock-1.3'
        compile 'org.spockframework.spock:spock-spring:spock-1.3'
}
```
3. For intermediate releases you can also use the commit-hash as version, e.g. compile `com.github.spockframework.spock:spock-core:d91bf785a1`

Modules
-------
* spock-core -- Core framework. This is the only mandatory module.
* spock-specs -- Specifications for spock-core, implemented using Spock. Not required for using Spock.
* spock-spring -- Integration with the [Spring TestContext Framework](https://docs.spring.io/spring/docs/4.1.5.RELEASE/spring-framework-reference/html/testing.html#testcontext-framework).
* spock-tapestry -- Integration with the [Tapestry 5](https://tapestry.apache.org/) IoC container.
* spock-guice -- Integration with [Guice](https://github.com/google/guice) 2/3.
* spock-unitils -- Integration with [Unitils](http://www.unitils.org/).
* spock-report -- Interactive, business-friendly HTML reports.

Building
--------

### Supported versions
Spock is supported for Java version 7, and 8 (with Groovy 2.5 Java 9+ are supported as well).

Spock is supported for Groovy version 2.4+

The tests are testing spock with a specific versions (variants) of groovy. Default is groovy version 2.4

The groovy 2.4 and 2.5 variant should pass on all supported JDK versions:

```
./gradlew clean build
```

(Windows: `gradlew clean build`).
All build dependencies, including
the [build tool](https://www.gradle.org) itself, will be downloaded
automatically (unless already present).

Contributing
------------
Contributions are welcome! Please see the [contributing page](https://github.com/spockframework/spock/blob/master/CONTRIBUTING.md) for detailed instructions.

Support
-------
If you have any comments or questions, please direct them to the [user forum](http://forum.spockframework.org).
All feedback is appreciated!

Java 9 Module Names
-------------------

All published jars (beginning with Spock 1.2) will contain Automatic-Module-Name manifest attribute. This allows for Spock to be
used in a Java 9 Module Path.

* spock-core -- `org.spockframework.core`
* spock-spring -- `org.spockframework.spring`
* spock-tapestry -- `org.spockframework.tapestry`
* spock-guice -- `org.spockframework.guice`
* spock-unitils -- `org.spockframework.unitils`

So module authors can use well known module names for the spock modules, e.g. something like this:
```
open module foo.bar {
  requires org.spockframework.core;
  requires org.spockframework.spring;
}
```

Links
-----
* Spock Homepage -- http://spockframework.org
* Spock Web Console -- http://webconsole.spockframework.org
* GitHub Organization -- http://github.spockframework.org
* Reference Documentation -- http://docs.spockframework.org
* Old Wiki -- http://wiki.spockframework.org
* Javadoc -- http://javadoc.spockframework.org
* User Forum -- http://forum.spockframework.org
* Developer Forum -- http://dev-forum.spockframework.org
* Issue Tracker -- http://issues.spockframework.org
* Build Server -- http://builds.spockframework.org
* Spock Example Project -- https://github.com/spockframework/spock-example
* Twitter -- http://twitter.spockframework.org

Live Long And Prosper!

The Spock Framework Team
