
# Maven

ABOUT

## Prerequisites

Maven is written in Java, thus the [Java installation](https://github.com/marcopaglio/installation-guides/tree/java#installation-guide "Installation guide for Java") is required.

## Installation Guide

The installation guide depending on your operating system.

### Windows

First of all check if Maven is already installed by running on the Command Prompt:
```
mvn -version
```
The output should be similar to the below:
```
Apache Maven 3.8.7 (b89d5959fcde851dcb1c8946a785a163f14e1e29)
Maven home: C:\Program Files\apache-maven-3.8.7
Java version: 11, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-11
Default locale: it_IT, platform encoding: Cp1252
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```
Instead, if `mvn` is not recognized as command or the version is not the desired one, then:
- choose the latest version from the [Maven official webpage](https://maven.apache.org/download.cgi "Downloading from Apache Maven webpage"), or another one from the [Apache Maven repository](https://repo.maven.apache.org/maven2/org/apache/maven/apache-maven/ "Downloading from Apache Maven repository").
- select the Maven binary zip file (e.g: `apache-maven-3.8.6-bin.zip`) to download it.
- if it doesn't already exist, create a new folder named `Apache Maven` or `Maven` in `C:\Program Files`.
- extract the downloaded archive in the Maven folder (it requires administrator permissions).

Let's call the Maven full path (e.g: `C:\Program Files\Apache Maven\apache-maven-3.8.6-bin`) as `<MVN_PATH>`.

Once done, set the `MAVEN_HOME` and `Path` environment variables that point to the same Maven installation to avoid inconsistencies and to decide which Maven version an application uses.

#### MAVEN_HOME

`MAVEN_HOME` environment variable has to be set to the previously defined `<MVN_PATH>`. You can do it by running the following command on Command Prompt as Administrator:
```
setx MAVEN_HOME <MVN_PATH> -m
```
You can check the actual value by running `echo $env:MAVEN_HOME` in *another* Command Prompt.<br>

Alternatively, you can do the same thing manually: **System** > **Advanced System Settings** > **Environment Variables...** > in the lower list (*System variables*) find the entry named `MAVEN_HOME` and click **Edit...** if it exists, or click **New...** if it doesn't exist > write `MAVEN_HOME` in Name and choose `<MVN_PATH>` for Value > confirm changes. The `MAVEN_HOME` value is now changed or added.

> :alarm_clock: **N.B**: The top list (*User variables*) should not contain any Maven-related entries. Delete them if you find them.

#### Path

In the `Path` environment variable has to be added the `%MAVEN_HOME%\bin` value: **System** > **Advanced System Settings** > **Environment Variables...** > in the lower list (*System variables*) find the entry named `Path` and click **Edit...** > **New** > write `%MAVEN_HOME%\bin` in the new line > confirm changes. The `Path` value is now changed.

### Linux

First of all check if Maven is already installed by running on the terminal:
```
mvn -version
```
The output should be similar to the below:
```
Apache Maven 3.8.6 (81a9f75f19aa7275152c262bcea1a77223b93445)
Maven home: /opt/apache-maven-3.8.6
Java version: 11.0.2, vendor: Oracle Corporation, runtime: /usr/lib/jvm/java-11-open-jdk-amd64
```
Otherwise, if something like `Command 'mvn' not found` appears, it means that Maven is not installed yet.<br>

If you have not version requirements, install Maven by simply running:
```
apt install maven -y
```

Otherwise, choose the desired version from the [Apache Maven repository](https://repo.maven.apache.org/maven2/org/apache/maven/apache-maven/ "Downloading from Apache Maven repository") and select the Maven binary tar.gz file (e.g: `apache-maven-3.8.6-bin.tar.gz`, let's call it `<BIN_FILE>`) to download it.<br>
Then, place yourself in the folder where the binary was downloaded, open a terminal and extract the archive in any directory (`/usr/local/` or `/opt/` are often used, let's call it `<MVN_DIR>`):
```
tar -xvf `<BIN_FILE>` -C <MVN_DIR>
```
If the destination directory doesn't exist (e.g. `/usr/local/apache-maven`), create it by running `mkdir -p <MVN_DIR>` before the extraction.<br>

Now, add the `bin` directory of the extracted archive (e.g: `/usr/local/apache-maven/apache-maven-3.8.6`, let's call it `<MVN_PATH>`) to the `PATH` environment variable. To make the change permanent, define it in the shell configuration file `.bashrc`. About that, open a terminal 
```
nano ~/.bashrc
```
Edit it by adding Maven-specific lines at the beginning of the file:
```
export M2_HOME=<MVN_PATH>
export M2=$M2_HOME/bin
export MAVEN_OPTS="-Xms256m -Xmx512m"
export PATH=$M2:$PATH
```
Once saved, we can reload the environment configuration without restarting:
```
source ~/.bashrc
```
Finally, we can verify the PATH environment variable contains `<MVN_PATH>/bin` through `echo $PATH`, and if Maven has been added through `mvn -version`.
