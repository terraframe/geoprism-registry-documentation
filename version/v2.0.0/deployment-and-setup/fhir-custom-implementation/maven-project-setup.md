# Maven project setup

Create a new Maven project that depends on `georegistry-server`. Geoprism Registry runs on Java 17, so compile your project for Java 17.

* Set `georegistry.version` to the version of Geoprism Registry you're deploying to.
* Use `provided` scope for `georegistry-server`, because the server already includes it at runtime.
* Add Terraframe's public Maven repositories, where the Geoprism Registry artifacts are published.

```xml
<project
  xmlns="http://maven.apache.org/POM/4.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.terraframe</groupId>
  <artifactId>fhir-implementation</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>jar</packaging>

  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
    <!-- The version of Geoprism Registry you're deploying to -->
    <georegistry.version>REPLACE_WITH_VERSION</georegistry.version>
  </properties>

  <repositories>
    <repository>
      <id>terraframe-geoprism-registry</id>
      <url>https://dl.cloudsmith.io/public/terraframe/geoprism-registry/maven/</url>
    </repository>
    <repository>
      <id>terraframe-geoprism</id>
      <url>https://dl.cloudsmith.io/public/terraframe/geoprism/maven/</url>
    </repository>
    <repository>
      <id>terraframe-runwaysdk</id>
      <url>https://dl.cloudsmith.io/public/terraframe/runwaysdk/maven/</url>
    </repository>
    <repository>
      <id>terraframe-public</id>
      <url>https://dl.cloudsmith.io/public/terraframe/public/maven/</url>
    </repository>
  </repositories>

  <dependencies>
    <dependency>
      <groupId>net.geoprism</groupId>
      <artifactId>georegistry-server</artifactId>
      <version>${georegistry.version}</version>
      <scope>provided</scope>
    </dependency>
  </dependencies>

  <build>
    <plugins>
      <plugin>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.13.0</version>
      </plugin>
    </plugins>
  </build>
</project>
```
