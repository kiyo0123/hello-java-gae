# hello-java-gae

https://cloud.google.com/appengine/docs/standard/java/tools/maven


## Generate Skelton Project by using maven
```
mvn archetype:generate -Dappengine-version=1.9.67 -Djava8=true -DCloudSDK_Tooling=false -Dapplication-id=$PROJECT -Dfilter=com.google.appengine.archetypes:
```
select `2` (remote -> com.google.appengine.archetypes:appengine-skeleton-archetype)

for version, just enter to select default most recent version.

set required properties as below : 
```
groupId: com.mycompany.myapp
artifactId: hello-java-gae
version: 1.0-SNAPSHOT
package: myapp
CloudSDK_Tooling: false
appengine-version: 1.9.67
application-id: fukudak-java
java8: true
service: default

```

confirm generated files and directories. 
```
tree .
.
├── README.md
└── hello-java-gae
    ├── README.md
    ├── nbactions.xml
    ├── pom.xml
    └── src
        ├── main
        │   ├── java
        │   │   └── myapp
        │   │       └── HelloAppEngine.java
        │   └── webapp
        │       ├── WEB-INF
        │       │   ├── appengine-web.xml
        │       │   ├── logging.properties
        │       │   └── web.xml
        │       └── index.jsp
        └── test
            └── java
                └── myapp
                    └── HelloAppEngineTest.java
```

## Test in Local

```
mvn clean package
```

```
mvn appengine:devserver -Dproject=$PROJECT
```

## Deploy to AppEngine




