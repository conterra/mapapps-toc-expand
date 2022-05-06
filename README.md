⚠️ This bundle is no longer needed in map.apps 4.13 or later.
See https://demos.conterra.de/mapapps/resources/jsregistry/root/toc/latest/README.md#how-to-expand-layers-in-toc-widget

# Toc Expand Bundle

## Installation Guide
**Requirement: map.apps 4.8.0**

[dn_tocexpand Documentation](https://github.com/conterra/mapapps-toc-expand/tree/master/src/main/js/bundles/dn_tocexpand)

## Development Guide
### Define the mapapps remote base
Before you can run the project you have to define the mapapps.remote.base property in the pom.xml-file:
`<mapapps.remote.base>http://%YOURSERVER%/ct-mapapps-webapp-%VERSION%</mapapps.remote.base>`

### Other methods to to define the mapapps.remote.base property.
1. Goal parameters
`mvn install -Dmapapps.remote.base=http://%YOURSERVER%/ct-mapapps-webapp-%VERSION%`

2. Build properties
Change the mapapps.remote.base in the build.properties file and run:
`mvn install -Denv=dev -Dlocal.configfile=%ABSOLUTEPATHTOPROJECTROOT%/build.properties`
