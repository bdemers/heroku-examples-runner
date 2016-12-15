Apache Shiro Example Runner
===========================

Deploy a Maven based war or Spring-Boot jar artifact to Heroku.  This project is intended to enable simple way to bootstrap an example application to Heroku.
The pom.xml will download a war/jar artifact and run that with an appropriate runner.

Example:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/bdemers/heroku-examples-runner&env\[ARTIFACT_ID\]=samples-spring-boot-web&&env\[RUNNER\]=spring-boot)

Heroku requires an app.json at root of a git repo (not a bad requirement), but we (and other projects) have a lot of examples in 
a Maven sub-module typically named `examples`.  This repo will wrap any Maven `war` or Spring-Boot `jar` project and download the latest release and run it.

Button format:

``` markdown
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/stormpath/heroku-war-runner&env\[GROUP_ID\]=<maven-groupId-here>&env\[ARTIFACT_ID\]=<maven-artifactId-here>)
```

Where `<maven-groupId-here>` is your groupId, and `<maven-artifactId-here>` is your artifactId.

Supported URL parameters:

| Parameter | Default Value | Description |
| --------- | ------------- | ----------- |
| `env[GROUP_ID]` | org.apache.shiro.samples | Artifact's group ID |
| `env[ARTIFACT_ID]` | N/A | Artifact's ID |
| `evn[VERSION]` | [0.0.0,) | Artifact's version (Version ranges are bad, but typically you will want to run the latest example)|
| `evn[RUNNER]` | jetty | `jetty`, `tomcat` or `spring-boot` |
