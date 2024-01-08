
# Java

[Java technology](https://docs.oracle.com/javaee/6/firstcup/doc/gkhoy.html) is both a programming language and a platform. The *Java programming language* is a high-level object-oriented language that has a particular syntax and style. A *Java platform* is a particular environment in which Java programming language applications run.<br>

There are three main components of Java programming language:

- The **Java virtual machine** (JVM) is a virtual machine that enables a computer to run Java programs as well as programs written in other languages that are also compiled to Java bytecode.

- The **Java Runtime Environment** (JRE) is a package of everything necessary to run a compiled Java program, including the JVM, the Java Class Library, the java command, and other infrastructure. However, it cannot be used to create new programs.

- The **Java Development Kit** (JDK) is the full-featured for Java. It has everything the JRE has, but also the compiler (javac) and tools (like javadoc and jdb) for creating and compiling Java source code.

There are four platforms of the Java programming language, each of which consists of a JVM and an API:

- **Standard Edition** (Java SE) provides APIs for core functionalities of the Java programming language, from the basic types and objects to high-level classes that are used for networking, security, database access, GUI development, and XML parsing. In addition to the core API, the Java SE platform consists of a virtual machine, development tools, deployment technologies, and other class libraries and toolkits commonly used in Java technology applications.

- **Enterprise Edition** (Java EE) is built on top of the Java SE platform and provides an API and runtime environment for developing and running large-scale, multi-tiered, scalable, reliable, and secure network applications.

- **Micro Edition** (Java ME) provides an API and a small-footprint virtual machine for running Java programming language applications on small devices, like mobile phones. The API is a subset of the Java SE API.

- **JavaFX** is used for creating rich internet applications using a lightweight user-interface API. JavaFX applications use hardware-accelerated graphics and media engines to take advantage of higher-performance clients and high-level APIs for connecting to networked data sources.

## Installation Guide

The installation guide depending on your operating system.

### Windows

First of all, run the following command on terminal:
```
java -version
```
If something like `openjdk version "xx"` appears, where `xx` is a number, then you already have Java installed.<br>
Instead, if `java` is not recognize as command or the major version `xx` is not the desired one, then:
- Download the Java binary zip file from [Oracle](https://www.oracle.com/java/technologies/downloads/archive/) or [OpenJDK](https://jdk.java.net/archive/) archives.
- Extract the archive (let's call it `<ARCHIVE_NAME>`) in `C:\Program Files\Java`.

Once done, set the `JAVA_HOME` and `Path` environment variables that point to the same Java installation to avoid inconsistencies and to decide which Java version an application uses.

#### JAVA_HOME

`JAVA_HOME` environment variable has to be set to `C:\Program Files\Java\<ARCHIVE_NAME>`, where `<ARCHIVE_NAME>` is the extracted zip file name. You can do it by running the following command on Command Prompt as Administrator:
```
setx JAVA_HOME C:\Program Files\Java\<ARCHIVE_NAME> -m
```
You can check the actual value by running `echo $env:JAVA_HOME` in *another* Command Prompt.<br>

Alternatively, you can do the same thing manually: **System** > **Advanced System Settings** > **Environment Variables...** > in the lower list (*System variables*) find the entry named `JAVA_HOME` and click **Edit...** if it exists, or click **New...** if it doesn't exist > write `JAVA_HOME` in Name and choose `C:\Program Files\Java\<ARCHIVE_NAME>` for Value > confirm changes. The `JAVA_HOME` value is now changed or added.

> :alarm_clock: **N.B**: The top list (*User variables*) should not contain any Java-related entries. Delete them if you find them.

#### Path

In the `Path` environment variable has to be added the `%JAVA_HOME%\bin` value: **System** > **Advanced System Settings** > **Environment Variables...** > in the lower list (*System variables*) find the entry named `Path` and click **Edit...** > **New** > write `%JAVA_HOME%\bin` in the new line > confirm changes. The `Path` value is now changed.

Moreover, delete the following values under `Path` if they exist:
- `C:\ProgramData\Oracle\Java\javapath`
- `C:\Program Files (x86)\Common Files\Oracle\Java\javapath`

### Linux

If your aim is only running Java programs on Linux, you only need to install the JRE. Instead, if you are planning to do some Java programming, you need to install the JDK. 

#### JRE

First of all, run the following command on terminal:
```
java -version
```
If something like `openjdk version "xx.yy.zz"` appears, where `xx`, `yy` and `zz` are numbers, then you already have a JRE installed.<br>
Instead, if `Command 'java' not found` appears or the major version `xx` is not the desired one, then install the JRE with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jre
```
You have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).

#### JDK

First of all, run the following command on terminal:
```
javac --version
```
If something like `javac xx.yy.zz` appears, where `xx`, `yy` and `zz` are numbers, then you already have a JDK installed.<br>
Instead, if `Command 'javac' not found` appears or the major version `xx` is not the desired one, then install the JDK with:
```
sudo apt-get update && sudo apt install openjdk-<XX>-jdk
```
You have to replace `<XX>` with the desired major version (e.g. `1.8`, `11`, `17`, etc.).
