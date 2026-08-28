
# Localoutlier process description (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.localoutlier.processDescription` *v1.0*

Process description for the localoutlier process

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Localoutlier process description
#### json
```json
{
  "version": "0.1",
  "id": "localoutlier",
  "title": "Local outlier factor (LOF)",
  "description": "The local outlier factor (LOF) algorithm computes a score indicating the degree of abnormality of each input observation.",
  "jobControlOptions": ["sync-execute", "async-execute"]
}
```

#### jsonld
```jsonld
{
  "@context": "https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/context.jsonld",
  "version": "0.1",
  "id": "localoutlier",
  "title": "Local outlier factor (LOF)",
  "description": "The local outlier factor (LOF) algorithm computes a score indicating the degree of abnormality of each input observation.",
  "jobControlOptions": [
    "sync-execute",
    "async-execute"
  ]
}
```

#### ttl
```ttl
@prefix dct: <http://purl.org/dc/terms/> .
@prefix proc: <https://w3id.org/ogc/api/processes/> .

<file:///github/workspace/localoutlier> dct:description "The local outlier factor (LOF) algorithm computes a score indicating the degree of abnormality of each input observation." ;
    dct:hasVersion "0.1" ;
    dct:title "Local outlier factor (LOF)" ;
    proc:jobControlOptions "async-execute",
        "sync-execute" .


```

## Schema

```yaml
allOf:
- $ref: https://ogcincubator.github.io/bblocks-ogcapi-processes/build/annotated/api/processes/v1/schemas/process/schema.yaml
- properties:
    inputs:
      $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputDescription/schema.yaml
      additionalProperties: false
    outputs:
      $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputDescription/schema.yaml
      additionalProperties: false
x-jsonld-extra-terms:
  id: '@id'
  version: http://purl.org/dc/terms/hasVersion
  title: http://purl.org/dc/terms/title
  description: http://purl.org/dc/terms/description
  jobControlOptions: https://w3id.org/ogc/api/processes/jobControlOptions

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "description": "dct:description",
    "title": "dct:title",
    "id": "@id",
    "jobControlOptions": "proc:jobControlOptions",
    "version": "dct:hasVersion",
    "nullable": "proc:nullable",
    "type": "proc:type",
    "$ref": {
      "@id": "proc:ref",
      "@type": "@id"
    },
    "default": {
      "@id": "proc:default",
      "@type": "@json"
    },
    "enum": {
      "@id": "proc:enum",
      "@container": "@set"
    },
    "minOccurs": "proc:minOccurs",
    "maxOccurs": "proc:maxOccurs",
    "dct": "http://purl.org/dc/terms/",
    "proc": "https://w3id.org/ogc/api/processes/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/localoutlier/processDescription`

