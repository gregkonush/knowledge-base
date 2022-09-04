---
id: 8tcalp6q5nfrdv9hbogt6i9
title: Gradle
desc: ''
updated: 1662328150708
created: 1662327934486
---

Simple Kotlin application in Gradle

In build.gradle.kts

```kotlin
/*
 * Setup application and kotlin plugins
 */

plugins {
  application
  kotlin("jvm") version "1.7.10"
}

application {
  mainClass.set("MainKt")
}

repositories {
  mavenCentral()
}

dependencies {

}

```
