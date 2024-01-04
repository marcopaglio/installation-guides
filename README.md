
# Maven

ABOUT

### Installation Guide

The installation guide depending on your operating system.

#### Linux

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
Otherwise, if something like `Command 'mvn' not found` appears, Maven is not installed yet.<br>

If you have not version requirements you can install Maven by simply running:
```
apt install maven -y
```

Otherwise, choose the desired version from the [Apache Maven repository](https://repo.maven.apache.org/maven2/org/apache/maven/apache-maven/) and select the Maven binary tar.gz file (let's call it `<BIN_FILE>` e.g: `apache-maven-3.8.6-bin.tar.gz`) to download it.<br>
Then, place yourself in the folder where the binary was downloaded, open a terminal and extract the archive in any directory (`/usr/local/` or `/opt/` are often used, let's call it `<MVN_DIR>`):
```
tar -xvf `<BIN_FILE>` -C <MVN_DIR>
```
If the destination directory doesn't exist (e.g. `/usr/local/apache-maven`), create it by running `mkdir -p <MVN_DIR>` before the extraction.<br>

Now, add the `bin` directory of the extracted archive (e.g. `/usr/local/apache-maven/apache-maven-3.8.6/bin`) to the PATH environment variable. To make the change permanent, define the `$PATH` variable in the shell configuration file `.bashrc`. About that, open a terminal 
```
nano ~/.bashrc
```
Edit it by adding Maven-specific lines at the beginning of the file:
```
export M2_HOME=<MVN_DIR>
export M2=$M2_HOME/bin
export MAVEN_OPTS="-Xms256m -Xmx512m"
export PATH=$M2:$PATH
```
Once saved, we can reload the environment configuration without restarting:
```
source ~/.bashrc
```
Finally, we can verify the PATH environment variable contains `<MVN_DIR>` through `echo $PATH` and if Maven has been added through `mvn -version`.
