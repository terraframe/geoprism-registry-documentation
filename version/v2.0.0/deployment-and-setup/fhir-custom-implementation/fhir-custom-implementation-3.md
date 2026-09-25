# Register the implementations with the Java Services architecture

Create the following text files inside the `META-INF/services` folder of your project's resources directory (`src/main/resources/META-INF/services`). Only create the files for the kinds of implementation you wrote:

1.  `net.geoprism.registry.etl.fhir.FhirDataPopulator`, for export implementations
2.  `net.geoprism.registry.etl.fhir.FhirResourceProcessor`, for import implementations

<figure><img src="../../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Each file lists the fully qualified class names of your implementations, one per line:

```
com.terraframe.demo.DemoFhirDataPopulator
```

and

```
com.terraframe.demo.DemoFhirResourceProcessor
```

For more information on the Java services architecture see [ServiceLoader (Java SE 17)](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ServiceLoader.html).
