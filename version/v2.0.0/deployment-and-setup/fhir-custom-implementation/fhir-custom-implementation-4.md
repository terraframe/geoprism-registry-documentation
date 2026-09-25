# Deploy implementation to server

Geoprism Registry runs as a web application in Tomcat, inside the `terraframe/geoprism-registry` Docker image. Your JAR must be added to the web application's own library folder, `webapps/ROOT/WEB-INF/lib`, so that it can see the Geoprism Registry classes.

1.  Build the JAR, for example with `mvn package`.
2.  Add the JAR to `/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/` in the Geoprism Registry container. The simplest way is to build your own image based on the official one:

    ```dockerfile
    FROM terraframe/geoprism-registry:latest
    COPY fhir-implementation-0.0.1-SNAPSHOT.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
    ```

    Then use your image in place of `terraframe/geoprism-registry` in your `docker-compose.yml`.
3.  Restart the Geoprism Registry container.

Your implementation now appears in the **Implementation** list when you [create a FHIR synchronization](../../external-system-integration/synchronize-an-external-system/fhir-synchronization.md).
