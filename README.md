
# Java

The Java Runtime Environment (JRE) is a package of everything necessary to run a compiled Java program, including the Java Virtual Machine (JVM), the Java Class Library, the java command, and other infrastructure. However, it cannot be used to create new programs.<br>

The Java Development Kit (JDK) is the full-featured for Java. It has everything the JRE has, but also the compiler (javac) and tools (like javadoc and jdb) for creating and compiling Java source code.

## Installation Guide

The installation guide depending on your operating system.

### Linux

#### JRE

If your aim is only running Java programs on Linux, you only need to install the JRE. First of all run the following command on terminal:
```
java -version
```
If something like `openjdk version "xx.yy.zz"` appears, where `xx`, `yy` and `zz` are numbers, then you already have a JRE installed.<br>
Instead, if `Command 'java' not found` appears or the major version `xx` is not the desired one, then install the JRE with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jre
```
Where you have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).

#### JDK

Instead, if you are planning to do some Java programming, you need to install the JDK. First of all run the following command on terminal:
```
javac --version
```
If something like `javac xx.yy.zz` appears, where `xx`, `yy` and `zz` are numbers, then you already have a JDK installed.<br>
Instead, if `Command 'javac' not found` appears or the major version `xx` is not the desired one, then install the JDK with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jdk
```
Where you have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).

### Windows

First of all check with `java -version`.<br>

Download the binary from [Oracle](https://www.oracle.com/java/technologies/downloads/archive/) or [OpenJDK](https://jdk.java.net/archive/) archives.<br>

Extract files in `C:\Program Files\Java`.<br>

Delete the following entries under "Path" (if they exist):
- C:\ProgramData\Oracle\Java\javapath
- C:\Program Files (x86)\Common Files\Oracle\Java\javapath
Insert the following entry instead:
- %JAVA_HOME%\bin

Set `JAVA_HOME` with `C:\Program Files\Java\<ARCHIVE_NAME>` extracted.
