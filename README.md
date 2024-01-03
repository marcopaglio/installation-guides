
# Java

ABOUT

## Java Runtime Environment (JRE)

### What it is

TODO

### Installation Guide

The installation guide depending on your operating system.

#### Linux (Ubuntu)

First of all check if JRE is already installed by running the following commands on terminal:
```
java -version
```
If `Command 'java' not found` appears, then the JRE is not installed. Otherwise, it will appear something like `openjdk version "xx.yy.zz"`, where `xx`, `yy` and `zz` are numbers. `xx` is the major version and must be 11 or greater in order to have a JRE sufficiently new installed; if it is lower, then you have to follow next steps.<br>

Before installing any new package is raccomanded to update your package listing with the most recent information:
```
sudo apt-get update
```
Install the JRE with the following commands:
```
sudo apt install openjdk-11-jre
```
Now if you run `java --version` you obtain the desired output.

## Java Development Kit (JDK)

### What it is

TODO

### Installation Guide

The installation guide depending on your operating system.

#### Linux (Ubuntu)

First of all check if JDK is already installed by running the following commands on terminal:
```
javac --version
```
If it appears something like `javac 11.0.21`, then you have already installed java, and you have to pass to next part of tutorial (link on words).<br>
Otherwise, if there is another version (major versions are ok or not?), or something like `Command 'javac' not found`, then the JDK is not installed and you can proceed with the next steps.<br>

Before installing any new package is raccomanded to update your package listing with the most recent information:
```
sudo apt-get update
```
Install the JDK with the following commands:
```
sudo apt install openjdk-11-jdk
```
The Java Development Kit (JDK) provides the Java Runtime Environment (JRE), Java Virtual Machine (JVM) and utilities to develop Java source code.<br>

Now if you run `javac --version` you obtain the desired output.

**TODO:** set JAVA_HOME? Non importa
