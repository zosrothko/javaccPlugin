# JavaCC Compiler Plugin for Gradle 

Provides the ability to use [JavaCC](http://javacc.java.net/) via [Gradle](http://www.gradle.org/). If the 'java' plugin is also applied, JavaCompile tasks will depend upon the compileJavacc task.

## Installation

Simply grab the plugin from Maven Central:

Add the following lines to your `build.gradle` script:

```groovy
buildscript {
    repositories {
        mavenCentral()
    }
    dependencies {
        classpath group: 'ca.coglinc', name: 'javacc-gradle-plugin', version: '1.0.0'
    }
}
apply plugin: 'javacc'
```

## Building

To build, simply run the following command in the directory where you checked out the plugin source:

`gradle clean build`

## Usage

Place your JavaCC code into `src/main/javacc`.
The generated Java code will be  put under `./build/generated/javacc` and will be compiled as part of the Java compile.

## Compatibility

This plugin requires Java 5+.

It has been tested with Gradle 1.11. Please let us know if you have had success with other versions of Gradle.

## Signature

The artifacts for this plugin are signed using the [PGP key](http://pgp.mit.edu:11371/pks/lookup?op=get&search=0x321163AE83A4068A) for `jonathan.martel@coglinc.ca`.

## Changelog

### 1.0.0

Initial version with limited features. Simply generates JavaCC files to Java from a non-configurable location into a non-configurable location.
