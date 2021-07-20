# Template for Scout Plugins

[![Plugins](https://github.com/augmented-testing/single-plugin-template/actions/workflows/plugins.yml/badge.svg)](https://github.com/augmented-testing/single-plugin-template/actions/workflows/plugins.yml)

## Introduction

Scout is a tool using a novel approach we call Augmented Testing (AT) to simplify Visual GUI Testing (VGT).

This repository serves as a template to develop a plugin for Scout without the complete Scout environment.

The main repository for Scout can be found [here](https://github.com/augmented-testing/scout).

## Requirements

Scout is developed in Java and therefore requires the Java Runtime Environment (JRE).
JRE version 8 or later is suitable for running Scout.

### Build and Run

Build automation is accomplished using a Maven. Use the following Maven command:

- To **build** the plugin: `mvn compile`.
- To **build** the plugin and perform **tests**: `mvn test`.
- To **install** the plugin to an existing Scout installation: `mvn install`.

The installation path for the plugin can be adjusted in the `pom.xml` at the `maven-resources-plugin` configuration.

## Run Plugin with Scout

Copy the compiled class files either by executing  `mvn install` or manual copying to the plugin folder of your Scout installation.
If you don't have Scout installed yet, you can download it from the [main repository](https://github.com/augmented-testing/scout).

## Plugin Development

Scout is a highly customizable tool due its plugin architecture. If you want to extend Scout's functionalities use this repository as a template for your new plugin or just create a new Java file within the `plugin/` folder of your Scout installation.

A plugin should be independent and therefore should not contain any external dependencies. But if necessary, external libs must be copied to the `bin/` directory of the Scout installation.

We emphasize a Keep it Simple/Stupid (KISS) approach to plugin development.

If you have to mange multiple Java versions you could use the tool [SDKMAN](https://sdkman.io) which helps to maintain multiple JDK versions.

### VSCode

If you decide to use VSCode as IDE than you have to install the [Java Extension Pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) to be able to develop a plugin.

You can find more information about how to manage Java projects in VSCode following this [link](https://code.visualstudio.com/docs/java/java-project).

## License

Copyright (c) 2021 Andreas Bauer

This work (source code) is licensed under [MIT](./LICENSES/MIT.txt).

Files other than source code are licensed as follows:

- Documentation and screenshots are licensed under [CC BY-SA 4.0](./LICENSES/CC-BY-SA-4.0.txt).

See the [LICENSES](./LICENSES/) folder in the root of this project for license details.
