# Deprecation notice

Do not use this sample. It's a reference on why page objects will burn your house. Gauge recommends **not** using page objects.
Refer https://github.com/getgauge-examples/gauge-active-admin-example-maven and our [blog](https://blog.getgauge.io/are-page-objects-anti-pattern-21b6e337880f)

# Gauge example in Java

[![Build Status](https://travis-ci.org/getgauge-examples/java-gradle-selenium.svg?branch=master)](https://travis-ci.org/getgauge-examples/java-gradle-selenium)

This is an example project for doing web automation testing with [Gauge](http://getgauge.io). This project tests some of the functionalities of the [active admin demo](https://github.com/getgauge/activeadmin-demo) app. This app is hosted as a Java WAR (with embedded Jetty). 

## Running this example
The tests are run on Chrome by default.

### Prerequisites

This example requires the following software to run.
  * [Java 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) or above
  * [Gauge](https://gauge.org/getting-started-guide/we-start/index.html)
  * Gauge Java plugin
    * can be installed using `gauge install java`
  * Chrome
  
### Setting up the System Under Test (SUT)

* Download [activeadmin-demo.war](https://bintray.com/artifact/download/gauge/activeadmin-demo/activeadmin-demo.war)
* Bring up the SUT by executing the below command
```
java -jar activeadmin-demo.war
```
* The SUT should now be available at [http://localhost:8080/](http://localhost:8080)

## Run specs

If you already have Gradle installed, you can execute specs as `gradle gauge`. Otherwise, you can use the gradle wrapper and run specs as below:

### On Linux / Mac

```
./gradlew gauge
```

### On Windows

```
gradlew.bat gauge
```
This runs Gauge specs with [Gradle](http://gradle.org).

This uses Chrome as default browser for specs execution. Make sure Chrome is installed in your machine and [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) is in PATH.

If you want to use Firefox/IE as browser, pass the corresponding argument to set browser environment as follows:

```
./gradlew gauge -Penv=firefox
or
./gradlew gauge -Penv=ie
```

Note:
  * Gauge can also be used with other [build tools](https://docs.gauge.org/latest/configuration.html#build-tools) like maven and Ant.
  * You can use Gauge even without a build script!

## Topics covered in the example

* [Specification](https://docs.gauge.org/latest/writing-specifications.html#specifications-spec), [Scenario](https://docs.gauge.org/latest/writing-specifications.html#scenario),  [Step](https://docs.gauge.org/latest/writing-specifications.html#step), [Concepts](https://docs.gauge.org/latest/writing-specifications.html#concepts) and [Context Steps](https://docs.gauge.org/latest/writing-specifications.html#longstart-context)
* [Table parameters](https://docs.gauge.org/latest/writing-specifications.html#table-parameters)
* Using [External datasource (special param)](https://docs.gauge.org/latest/writing-specifications.html#special-parameters)
* Using [tags](https://docs.gauge.org/latest/writing-specifications.html#tags)
* Using Gauge with [Selenium Webdriver](http://docs.seleniumhq.org/projects/webdriver/)
* Running Gauge specs with [Gradle](http://gradle.org)

# Copyright
Copyright 2019, ThoughtWorks Inc.
