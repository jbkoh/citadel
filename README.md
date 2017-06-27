# Citadel With Vert.X

This is a Maven project. You can use any mvn commands.

### Set up dev env.
```{r, engine='bash', count_lines}
mvn eclipse:eclipse
```

### Test Comma
```{r, engine='bash', count_lines}
mvn test
```

### Packaging
```{r, engine='bash', count_lines}
mvn clean package
```

### Naviation
1. MainVerticle contains all the verticles to be deployed (currently only one.)
2. model package contains data model we will use. It will be shared across different packages.
3. timeseries package is not used for now.
4. Best practice is to use different verticles for different services and then do port-forwarding to 80. Currently all APIs should be collected in RestApi Verticle.

### (For Dev) Add your module?
1. If you would like to add a module, add a package with the same structure of metadata and metadata.impl.
2. RestApi.java routes all functions in the modules in 1. to appropriate URLs. (This is not the best practice but it seems to be a way only with a verticle. Suggestion?)


