
# Example OGC API Processes instance input descriptions (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.inputDescriptions` *v1.0*

Collection of input descriptions

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
anyOf:
- $ref: https://Geonovum-labs.github.io/ospd-dtaas-register/build-local/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputDescription/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://Geonovum-labs.github.io/ospd-dtaas-register/build-local/annotated/dtaas/ogcapi/processes/schemas/inputDescriptions/schema.json)
* JSON version: [schema.json](https://Geonovum-labs.github.io/ospd-dtaas-register/build-local/annotated/dtaas/ogcapi/processes/schemas/inputDescriptions/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@vocab": "https://w3id.org/ogc/api/processes/",
    "maxOccurs": "proc:maxOccurs",
    "minOccurs": "proc:minOccurs",
    "schema": {
      "@context": {
        "@vocab": "https://w3id.org/ogc/api/schema/"
      },
      "@id": "proc:schema"
    },
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
[context.jsonld](https://Geonovum-labs.github.io/ospd-dtaas-register/build-local/annotated/dtaas/ogcapi/processes/schemas/inputDescriptions/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/inputDescriptions`

