# What is Maven?
Maven is a project management tool, A build tool such as Ant is focused solely on preprocessing, compilation, packaging, testing, and distribution. on the other hand maven provides the super set of features found in build tool. In addition to providing build capabilities, Maven can also run reports, generate a web site, and facilitate communication among members of a working team.

A more formal definition of Apache Maven: Maven is a project management tool which encompasses a project object model, a set of standards, a project lifecycle, a dependency management system, and logic for executing plugin goals at defined phases in a lifecycle. When you use Maven, you describe your project using a well-defined project object model, Maven can then apply cross-cutting logic from a set of shared (or custom) plugins.

# Convention Over Configuration
Convention over configuration is a simple concept. Systems, libraries, and frameworks should assume reasonable defaults. Without requiring unnecessary configuration, systems should “just work”. Maven incorporates sensible default behavior for projects Without customization, source code is assumed to be in ${basedir}/src/main/java and resources are assumed to be in ${basedir}/src/main/resources. Tests are assumed to be in ${basedir}/src/test, and a project is assumed to produce a JAR file. Maven assumes that you want the compile byte code to ${basedir}/target/classes and then create a distributable JAR file in ${basedir}/target.

If you follow the conventions, Maven will require almost zero effort - just put your source in the correct directory, and Maven will take care of the rest.

If you don’t care to follow convention, Maven will allow you to customize defaults in order to adapt to your specific requirements.

# The POM - Project Object Model

The POM is where a project’s identity and structure are declared, builds are configured, and projects are related to one another. The presence of a pom.xml file defines a Maven project.
The pom.xml is structured in to 4 parts as shown below

"
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
<!-- Basics -->
           <groupId>com.example</groupId>
           <artifactId>my-app</artifactId>
           <version>1.0.0-SNAPSHOT</version>
           <packaging>pom<packaging>
           <description>This is pom.xml documentation </description>
        <modules>
            <module>tachyon-pom</module>
        </modules>
    <parent>
           <groupId>org.springframework.boot</groupId>
           <artifactId>spring-boot-starter-parent</artifactId>
           <version>2.5.8</version>
           <relativePath /> <!-- lookup parent from repository -->
    </parent>
    <properties>
           <java.version>11</java.version>
           <tdp.version>${project.version}</tdp.version>
           <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
           <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
           <imageVersion>SNAPSHOT</imageVersion>
           <dockerImageName>${project.artifactId}</dockerImageName>
           <openJdkImage>openjdk:13.0.2-jdk-slim</openJdkImage>
           <year>2023</year>
           <dockerfile.skip>true</dockerfile.skip>
    </properties>
    <dependencyManagement>
         <dependencies>
                <!-- Spring -->
                <!-- Spring AOP + AspectJ -->
                <!-- Google -->
                <!-- Apache -->
                <!-- Object Mappers -->
                <!-- Logging -->
                <!-- InHouse -->
                <!-- Others -->
                <!-- Test -->
         </dependencies>
    </dependencyManagement>

  <!-- Build Settings -->
<build>
    <pluginManagement>
    <plugins>
        <!-- Basic plugins -->
        <!-- Quality Plugins -->
        <!-- Report Plugins -->
        <!-- Docker -->
        <!-- Release -->
    </plugins>
    </pluginManagement>
</build>
<!-- Reports -->
    <reporting>
        <plugins>
        </plugins>
    </reporting>
<!-- Project Information -->
    <url></url>
    <inceptionYear>2023</inceptionYear>
    <developers>
        <developer>
            <id>3161478</id>
            <name>Pavan Katukala</name>
            <email>pakatuka@lowes.com</email>
            <roles>
                <role>developer</role>
            </roles>
        </developer>
    </developers>
    <!-- Environment Settings -->
    <scm>
        <connection></connection>
        <developerConnection></developerConnection>
        <url></url>
        <tag>tachyon-plaza</tag>
    </scm>
<profiles>
</profiles>
</project>
"

