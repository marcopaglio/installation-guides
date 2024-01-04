
# Java

ABOUT

## Java Runtime Environment (JRE)

TODO

### Installation Guide

The installation guide depending on your operating system.

#### Linux (Ubuntu)

First of all check if JRE is already installed by running the following command on terminal:
```
java -version
```
If something like `openjdk version "xx.yy.zz"` appears, where `xx`, `yy` and `zz` are numbers, then you already have a JRE installed.<br>
Instead, if `Command 'java' not found` appears or the major version `xx` is not the desired one, then install the JRE with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jre
```
Where you have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).

## Java Development Kit (JDK)

The Java Development Kit (JDK) provides the Java Runtime Environment (JRE), Java Virtual Machine (JVM) and utilities to develop Java source code.

### Installation Guide

The installation guide depending on your operating system.

#### Linux

Instead, if `Command 'java' not found` appears, or the major version `xx` is not the desired one, then install the JRE with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jre
```
Where you have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).

First of all check if JDK is already installed by running the following command on terminal:
```
javac --version
```
If something like `javac xx.yy.zz` appears, where `xx`, `yy` and `zz` are numbers, then you already have a JDK installed.<br>
Instead, if `Command 'javac' not found` appears or the major version `xx` is not the desired one, then install the JDK with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jdk
```
Where you have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).

**TODO:** set JAVA_HOME
