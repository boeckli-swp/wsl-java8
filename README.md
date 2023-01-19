# WSL Demo With JDK-8

## Requirement
- JDK-8
- Maven

## Build
- ```shell
  mvn clean package
  ```
- When running in wsl terminal assure that JDK-8 has been correctly. Underlying WSL-Distro is set probably to JDK-8.<br />
  ```shell
  export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/
  export PATH=$JAVA_HOME/bin:$PATH`
  ```
- Check Java version (should be Java 8):
  ```shell
  java -version
  ```
  ```console
  openjdk version "1.8.0_352"
  OpenJDK Runtime Environment (build 1.8.0_352-8u352-ga-1~22.04-b08)
  OpenJDK 64-Bit Server VM (build 25.352-b08, mixed mode)
  ```
- Check Maven version (should be Java 11):
  ```shell 
  mvn -version
  ```
  Output should be:
  ```console
  Apache Maven 3.6.3
  Maven home: /usr/share/maven
  Java version: 1.8.0_352, vendor: Private Build, runtime: /usr/lib/jvm/java-8-openjdk-amd64/jre
  Default locale: en, platform encoding: UTF-8
  OS name: "linux", version: "5.15.79.1-microsoft-standard-wsl2", arch: "amd64", family: "unix"
  ```

## Run
Currently does not run in IntellJ
See Bug: https://youtrack.jetbrains.com/issue/IDEA-303265/Maven-resources-compiler-error-occurs-when-trying-to-run-maven-configuration
```shell
/usr/lib/jvm/java-8-openjdk-amd64/bin -jar wsl-java8-1.0-SNAPSHOT-spring-boot.jar
```
or if JDK11 has been set correctly just
```shell
java -jar wsl-java8-1.0-SNAPSHOT-spring-boot.jar
```
