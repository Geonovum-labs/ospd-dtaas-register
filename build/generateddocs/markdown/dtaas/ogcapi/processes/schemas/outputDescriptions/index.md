
# Example OGC API Processes instance output descriptions (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.outputDescriptions` *v1.0*

Collection of output descriptions

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
anyOf:
- $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputDescription/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/outputDescriptions/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/outputDescriptions/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@vocab": "https://w3id.org/ogc/api/processes/",
    "schema": "proc:schema",
    "title": "dct:title",
    "description": "dct:description",
    "keywords": "proc:keywords",
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
    "minOccurs": "proc:minOccurs",
    "maxOccurs": "proc:maxOccurs",
    "enum": {
      "@id": "proc:enum",
      "@container": "@set"
    },
    "dct": "http://purl.org/dc/terms/",
    "proc": "https://w3id.org/ogc/api/processes/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/outputDescriptions/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/outputDescriptions`

