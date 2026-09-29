
# Validate Point Cloud process (Schema)

`geonovum.dtaas.ogcapi.processes.validate_point_cloud` *v1.0*

Process to validate point cloud data for OGC API Processes using the application package Validate Point Cloud.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Metadata description of Validate Point Cloud process
A process description using the APKG metadata profiles
#### ttl
```ttl
@prefix apkg: <http://w3id.org/apkg/terms#> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix schema: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix ex: <https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1#> .

ex:validate_point_cloud a apkg:ApplicationPackage ;
    dct:identifier "https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1" ;
    dct:title "Validate Point Cloud" ;
    dct:description "Check that the selected point clouds are ready to use." ;
    dct:issued "2025-12-17"^^xsd:date ;
    dct:modified "2025-12-17"^^xsd:date .
    
ex:validatePointCloudProcess a apkg:Process ;
    dct:type "CommandLineTool" ;
    apkg:hasInput ex:point_clouds ;
    apkg:hasOutput ex:validation_report .

ex:point_clouds a apkg:Parameter ;
    dct:identifier "point_clouds" ;
    dct:type "object" ;
    apkg:label "point_clouds" .

ex:validation_report a apkg:Parameter ;
    dct:identifier "validation_report" ;
    dct:type "object" ;
    apkg:label "validation_report" .

```


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/validate_point_cloud`

