## Component Catalog

This repo contains a [component-metadata.yaml](component-metadata.yaml) file that describes the components (e.g. services, databases, queues etc.) that belong
to this repo.  That YAML file is automatically read by the [Component Catalog](https://github.com/moneysupermarket/component-catalog) from this repo's
main branch every 15 minutes, with any changes merged to the main branch automatically appearing in the Component Catalog after 15-30 minutes.

### Checking the contents of the `component-metadata.yaml` file is valid after making a change

You can run the following command to validate the contents of the `component-metadata.yaml` file:

```shell
$ ./gradlew validateComponentMetadata
```

The following command can also be used:

```shell
$ ./gradlew build
```

### Changes to `component-metadata.yaml` file are automatically picked up by the Component Catalog

There is no need to release changes to the [component-metadata.yaml](component-metadata.yaml) file in this repo.
When changes to the [component-metadata.yaml](component-metadata.yaml) file are merged to the main branch,
those changes will automatically become visible in the Component Catalog within the next 15 to 30 minutes.  
The Component Catalog reloads all `component-metadata.yaml` files every 15 minutes but this takes 10 to 30
minutes to complete.

### Example YAML for areas, teams and components

See the https://github.com/moneysupermarket/component-metadata-codebase-template/blob/main/component-metadata.yaml
file for example YAML for components.

### Updating the dependency on the `com.moneysupermarket.componentcatalog:component-catalog-component-metadata` library

From time to time, the Component Catalog will make changes to the objects and fields that are supported in
`component-metadata.yaml` files. When this happens, you can bring in support for those changes to this repo by
updating the version of the `componentMetadataVersion` setting in the [gradle.properties](gradle.properties)
file in this repo.
