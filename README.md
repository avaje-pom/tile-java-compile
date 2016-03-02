# tile-java-compile
Maven tile for java compile

## Example use

```xml
      <!-- In maven build / plugins -->

      <plugin>
        <groupId>io.repaint.maven</groupId>
        <artifactId>tiles-maven-plugin</artifactId>
        <version>2.8</version>
        <extensions>true</extensions>
        <configuration>
          <tiles>
            <tile>org.avaje.tile:java-compile:1.1</tile>
            <tile>org.avaje.tile:kotlin-compile:1.1</tile>
            <tile>org.avaje.tile:ebean-enhancement:1.1</tile>
          </tiles>
        </configuration>
      </plugin>

```

## What it does

Effectively the java-compile tile brings in the *maven-compiler-plugin*

```xml

  <!-- defaults, override in your project pom if needed -->
  <properties>
    <java.version>1.8</java.version>
    <maven-compiler-plugin.version>3.5.1</maven-compiler-plugin.version>
  </properties>

 
  <!-- brought into build / plugins -->

      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>${maven-compiler-plugin.version}</version>
        <configuration>
          <source>${java.version}</source>
          <target>${java.version}</target>
        </configuration>
      </plugin>


```
