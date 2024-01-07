
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

#### Windows

First of all check with `java -version`.<br>

Download the binary from [Oracle](https://www.oracle.com/java/technologies/downloads/archive/) or [OpenJDK](https://jdk.java.net/archive/) archives.<br>

Extract files in `C:\Program Files\Java`.<br>

Delete the following entries under "Path" (if they exist):
- C:\ProgramData\Oracle\Java\javapath
- C:\Program Files (x86)\Common Files\Oracle\Java\javapath
Insert the following entry instead:
- %JAVA_HOME%\bin

Set `JAVA_HOME` with `C:\Program Files\Java\<ARCHIVE_NAME>` extracted.

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
