# My archetype

## Description

<p>This project is created to understand how to create a new archetype for Java with maven in local repository.</p>

<p>This archetype was able to create a simple Java structure project, with the next:</p>

```console
${artifactId}
pom.xml
README.md
|--src
    |--main
    |    |--java
    |        |--${package}
    |--test
        |--java
            |--${package}
```

---

## Configuration

<p>In order to work with this project you need to have install the next tools:</p>

- **Maven**
- **Java 8 or >**
- **Git**
- **IDE or VSC**

---

## How to work with this archetype

<p>You need to know the next:</p>

- <p>If you want to modify or add news files like classes .java, folders, and others you have to do all this in:</p>

```console
src
|--main
    |--resources
        |--archetype-resources
```

<p>And don't forget to verify or append the news files or structure in:</p>

```console
src
|--main
    |--resources
        |--META-INF
            |--maven
                |--archetype-metadata.xml
```

---

## What run the application?

<p>We can run the application in console following the next steps:</p>

1. To generate your first archetype with this project, you have to execute the command:

```console
mvn clean install
```

2. If the build was succesful you have to go in a empty folder and execute the command:

```console
mvn archetype:generate -DarchetypeGroupId=com.midominio \
                       -DarchetypeArtifactId=my-archetype \
                       -DarchetypeVersion=1.0.0 \
                       -DgroupId=[com.myapp] \
                       -DartifactId=[myapp-example] \
                       -Dversion=[1.0.0] \
                       -Dpackage=[com.miapp.demo] \
                       -DinteractiveMode=false
```

<p>Replace the information in brackets with your information. </p>