
# Convert Format process (Schema)

`geonovum.dtaas.ogcapi.processes.convert_format` *v0.1*

Process to convert point cloud data between supported formats using the application package Convert Format.

[*Status*](http://www.opengis.net/def/status): Under development

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

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/convert_format/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/convert_format/schema.yaml)


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
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/convert_format/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/convert_format`

