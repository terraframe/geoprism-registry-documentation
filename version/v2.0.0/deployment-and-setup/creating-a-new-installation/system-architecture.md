# System Architecture

Geoprism Registry is a Java web application. It runs in Docker as three containers:

| Container | Image | What it does |
| --------- | ----- | ------------ |
| Geoprism Registry | `terraframe/geoprism-registry` | The web application: Java 17 and Tomcat 11, running Geoprism Registry as a Spring Boot web application (WAR). Listens on port 8080. |
| PostgreSQL | `postgis/postgis` (PostgreSQL 18 with PostGIS 3.6) | Stores registry data and geometries. |
| OrientDB | `orientdb:3.2` | The graph database that stores Geo-Objects, their relationships and their history. |

<figure><img src="../../../../.gitbook/assets/GPR Docker Install Diagram (1).png" alt=""><figcaption></figcaption></figure>

The diagram shows the container layout. The software versions in it are older than those in the table above.

The [example docker-compose.yml](https://github.com/terraframe/geoprism-registry/blob/master/src/build/docker/georegistry/docker-compose.yml) file sets up an installation like this. It also stores the application's data in `/data/georegistry` and its logs in `/data/logs/tomcat` on the host.

Other services are optional and configured separately:

* An SMTP email server, for invitations and notifications. See [System email management](../system-email-management.md).
* A Mapbox access token, for the maps.
* An Apache Jena triple store, to receive published Spatial Knowledge Graphs. See [Apache Jena External System](../../external-system-integration/register-an-external-system/apache-jena-external-system.md).

The Geoprism Registry web application is built from these projects:

<table data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td></td><td><a href="https://github.com/terraframe/Runway-SDK">Runway SDK</a></td><td>-></td></tr><tr><td></td><td><a href="https://github.com/terraframe/geoprism">Geoprism</a></td><td>-></td></tr><tr><td></td><td><a href="https://github.com/terraframe/geoprism-registry">Geoprism Registry</a></td><td></td></tr><tr><td></td><td><a href="https://spring.io/">Spring MVC</a></td><td>-></td></tr></tbody></table>
