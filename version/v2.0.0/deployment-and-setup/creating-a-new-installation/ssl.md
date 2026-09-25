# SSL

Geoprism Registry uses HTTP on port 8080 by default. The Docker image doesn't configure HTTPS.

Set up SSL/HTTPS outside the Geoprism Registry container. The recommended way is a reverse proxy, such as nginx or Apache, that accepts HTTPS connections and forwards them to Geoprism Registry.

When Geoprism Registry is served over HTTPS, set its public URL (the `geoprism.remote.url` setting in `docker-compose.yml`) to the HTTPS address, so that links in emails and other generated URLs are correct.
