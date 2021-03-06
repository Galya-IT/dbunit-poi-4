**How to build the artifact**

* Download ojdbc6.jar from Oracle website.
* Install ojdbc6 to the local maven report (change the -Dfile location): 
```
mvn install:install-file -Dfile=lib\ojdbc6.jar -DgroupId=com.oracle -DartifactId=ojdbc6 -Dversion=11.2.0.3 -Dpackaging=jar
```

* Generate dbunit/target/dbunit-2.6.1-SNAPSHOT.jar

```
mvn -DskipTests=true package
```

* Upload to private artifact repo or install locally (change PATH):

```
mvn install:install-file -Dfile=${PATH}\dbunit-2.6.1-SNAPSHOT.jar -DgroupId=org.dbunit -DartifactId=dbunit -Dversion=2.6.1-SNAPSHOT 
-Dpackaging=jar
```
