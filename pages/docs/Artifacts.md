---
title: Artifacts
permalink: /artifacts.html
summary: ""
---

Ktor is divided into modules to allow fine-grained inclusion of dependencies based on the functionality required.
The typical Ktor application would require `ktor-server-core` and a corresponding engine depending on whether it's self-hosted
 or using an Application Server.

All artifacts in Ktor belong to `io.ktor` group and hosted on [Bintray](https://bintray.com/kotlin/ktor)

[![Download](https://api.bintray.com/packages/kotlin/ktor/ktor/images/download.svg?version={{site.ktor_version}})](https://bintray.com/kotlin/ktor/ktor/{{site.ktor_version}})

Ktor is split into several groups of modules:

* `ktor-server` contains modules that support running Ktor Application with different engines: Netty, Jetty, Tomcat, and
generic servlet. It also contains TestEngine for setting up application tests without starting real server.
  * `ktor-server-core` is a core package where most of the application API and implementation is located.
  * `ktor-server-jetty` support a deployed or embedded Jetty instance
  * `ktor-server-netty` supports Netty in an embedded mode
  * `ktor-server-tomcat` supports Tomcat servers
  * `ktor-server-servlet` is used by Jetty and Tomcat and allows running in generic servlet container
  * `ktor-server-test-host` allows running application tests faster without starting full host
* `ktor-features` groups modules for features that are optional and may not be required by every application
  * `ktor-auth` provides support for different authentication systems like Basic, Digest, Forms, OAuth 1a and 2
  * `ktor-auth-ldap` adds ability to authenticate against LDAP instance
  * `ktor-freemarker` integrates Ktor with Freemarker templates
  * `ktor-html-builder` integrates Ktor with kotlinx.html builders
  * `ktor-locations` contains experimental support for typed locations
  * `ktor-server-sessions` adds ability to use stateful sessions stored on a server
  * `ktor-websockets` provides support for Websockets


See instructions for setting up a project with

* [Maven](getting-started-maven)
* [Gradle](getting-started-gradle)
