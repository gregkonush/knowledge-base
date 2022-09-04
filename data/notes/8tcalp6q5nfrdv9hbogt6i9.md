
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
