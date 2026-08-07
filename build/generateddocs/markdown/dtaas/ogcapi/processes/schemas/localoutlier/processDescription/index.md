
# Localoutlier process description (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.localoutlier.processDescription` *v1.0*

Process description for the localoutlier process

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
allOf:
- $ref: https://ogcincubator.github.io/bblocks-ogcapi-processes/build/annotated/api/processes/v1/schemas/process/schema.yaml
- properties:
    inputs:
      $ref: https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputDescription/schema.yaml
      additionalProperties: false
    outputs:
      $ref: https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputDescription/schema.yaml
      additionalProperties: false

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
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
[context.jsonld](https://raw.githubusercontent.com/Geonovum-labs/ospd-dtaas-register/undefined/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/processDescription/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/localoutlier/processDescription`

