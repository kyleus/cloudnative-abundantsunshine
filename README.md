# cloud-native

## Java 11 Changes

### JAXBException

The libraries are no longer included in java 11

https://stackoverflow.com/questions/43574426/how-to-resolve-java-lang-noclassdeffounderror-javax-xml-bind-jaxbexception-in-j

Add jaxb libraries to parent pom
```xml
 <dependency>
     <groupId>javax.xml.bind</groupId>
     <artifactId>jaxb-api</artifactId>
     <version>2.2.11</version>
 </dependency>
 <dependency>
     <groupId>com.sun.xml.bind</groupId>
     <artifactId>jaxb-core</artifactId>
     <version>2.2.11</version>
 </dependency>
 <dependency>
     <groupId>com.sun.xml.bind</groupId>
     <artifactId>jaxb-impl</artifactId>
     <version>2.2.11</version>
 </dependency>
 <dependency>
     <groupId>javax.activation</groupId>
     <artifactId>activation</artifactId>
     <version>1.1.1</version>
 </dependency>
```

### Hibernate Mapping Exception
org.hibernate.MappingException: Could not get constructor for org.hibernate.persister.entity.SingleTableEntityPersister

https://stackoverflow.com/questions/52913597/springboot-org-hibernate-mappingexception-could-not-get-constructor-for-org-hi

Add javassist to the parent pom:

```xml
<dependency>
    <groupId>org.javassist</groupId>
    <artifactId>javassist</artifactId>
    <version>3.23.2-GA</version>
</dependency>
```