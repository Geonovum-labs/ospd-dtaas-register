
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


### Metadata description of Validate Point Cloud process in json
A process description using the APKG metadata profiles
#### json
```json
 {
  "id": "https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1",
  "type": "apkg:ApplicationPackage",

  "dct:identifier":   "https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1",
  "dct:title":        "Validate Point Cloud",
  "dct:description":  "Check that the selected point clouds are ready to use.",
  "dct:issued":       "2025-12-17",
  "dct:modified":     "2025-12-17",

  "apkg:hasInput":  [ "point_clouds" ],
  "apkg:hasOutput": [ "validation_report" ],

  "apkg:processes": [
    {
      "type": "apkg:Process",
      "dct:type": "CommandLineTool",
      "apkg:hasInput":  [ "point_clouds" ],
      "apkg:hasOutput": [ "validation_report" ]
    }
  ]
}

```

#### jsonld
```jsonld
{
  "@context": "https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/validate_point_cloud/context.jsonld",
  "id": "https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1",
  "type": "apkg:ApplicationPackage",
  "dct:identifier": "https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1",
  "dct:title": "Validate Point Cloud",
  "dct:description": "Check that the selected point clouds are ready to use.",
  "dct:issued": "2025-12-17",
  "dct:modified": "2025-12-17",
  "apkg:hasInput": [
    "point_clouds"
  ],
  "apkg:hasOutput": [
    "validation_report"
  ],
  "apkg:processes": [
    {
      "type": "apkg:Process",
      "dct:type": "CommandLineTool",
      "apkg:hasInput": [
        "point_clouds"
      ],
      "apkg:hasOutput": [
        "validation_report"
      ]
    }
  ]
}
```

#### ttl
```ttl
@prefix apkg: <http://w3id.org/apkg/terms#> .
@prefix dct: <http://purl.org/dc/terms/> .

<https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1> a apkg:ApplicationPackage ;
    dct:description "Check that the selected point clouds are ready to use." ;
    dct:identifier "https://processes.staging.roofer-online.nl/ogcapi/processes/roofer:validate_point_cloud:v1" ;
    dct:issued "2025-12-17" ;
    dct:modified "2025-12-17" ;
    dct:title "Validate Point Cloud" ;
    apkg:hasInput "point_clouds" ;
    apkg:hasOutput "validation_report" ;
    apkg:processes [ a apkg:Process ;
            dct:type "CommandLineTool" ;
            apkg:hasInput "point_clouds" ;
            apkg:hasOutput "validation_report" ] .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
allOf:
- $ref: https://nielshoffmann.github.io/registered-item-model/build/annotated/model/registered-item/rim/registered-item/schema.yaml
- properties:
    dct:identifier:
      type: string
      format: uri
      x-jsonld-id: http://purl.org/dc/terms/identifier
    dct:title:
      type: string
      x-jsonld-id: http://purl.org/dc/terms/title
    dct:description:
      type: string
      x-jsonld-id: http://purl.org/dc/terms/description
    dct:issued:
      type: string
      format: date
      x-jsonld-id: http://purl.org/dc/terms/issued
    dct:modified:
      type: string
      format: date
      x-jsonld-id: http://purl.org/dc/terms/modified
    apkg:hasInput:
      type: array
      items:
        type: string
      x-jsonld-id: http://w3id.org/apkg/terms#hasInput
    apkg:hasOutput:
      type: array
      items:
        type: string
      x-jsonld-id: http://w3id.org/apkg/terms#hasOutput
  required:
  - dct:identifier
  - dct:title
  - dct:issued
additionalProperties: true
x-jsonld-extra-terms:
  id: '@id'
  type: '@type'
x-jsonld-prefixes:
  rim: https://w3id.org/ogc/rim/
  dct: http://purl.org/dc/terms/
  skos: http://www.w3.org/2004/02/skos/core#
  prov: http://www.w3.org/ns/prov#
  apkg: http://w3id.org/apkg/terms#
  xsd: http://www.w3.org/2001/XMLSchema#
  schema: https://schema.org/

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/validate_point_cloud/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/validate_point_cloud/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "id": "@id",
    "type": "@type",
    "rim": "https://w3id.org/ogc/rim/",
    "dct": "http://purl.org/dc/terms/",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "prov": "http://www.w3.org/ns/prov#",
    "apkg": "http://w3id.org/apkg/terms#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "schema": "https://schema.org/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/validate_point_cloud/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/validate_point_cloud`

