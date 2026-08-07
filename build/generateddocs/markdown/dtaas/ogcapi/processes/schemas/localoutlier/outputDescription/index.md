
# Localoutlier process output description (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.localoutlier.outputDescription` *v1.0*

Output description for the localoutlier process

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
allOf:
- $ref: https://ogcincubator.github.io/bblocks-ogcapi-processes/build/annotated/api/processes/v1/schemas/outputDescription/schema.yaml
properties:
  schema:
    type: object
    properties:
      output_dataset:
        type: object
        properties:
          title:
            type: string
            const: Output Dataset
          description:
            type: string
            const: output
          schema:
            $ref: https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputSchema/schema.yaml#/properties/output_dataset

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputDescription/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputDescription/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@vocab": "https://w3id.org/ogc/api/processes/",
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
[context.jsonld](https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputDescription/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/localoutlier/outputDescription`

