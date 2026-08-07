
# Localoutlier process input description (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.localoutlier.inputDescription` *v1.0*

Input description for the localoutlier process

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
allOf:
- $ref: https://ogcincubator.github.io/bblocks-ogcapi-processes/build/annotated/api/processes/v1/schemas/inputDescription/schema.yaml
type: object
properties:
  dataset:
    type: object
    properties:
      title:
        type: string
        const: Dataset
      description:
        type: string
        const: geojson dataset of points, in one CRS, for which LOF scores should
          be computed.
      minOccurs:
        type: integer
        const: 1
      maxOccurs:
        type: integer
        const: 1
      schema:
        $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/schema.yaml#/properties/dataset
  n_neighbors:
    type: object
    properties:
      title:
        type: string
        const: Number of neighbors
      description:
        type: string
        const: Number of neighbors to use by default for `kneighbors` queries. If
          `n_neighbors` is larger than the number of samples provided, all samples
          will be used.
      minOccurs:
        type: integer
        const: 0
      maxOccurs:
        type: integer
        const: 1
      schema:
        $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/schema.yaml#/properties/n_neighbors
  leaf_size:
    type: object
    properties:
      title:
        type: string
        const: Leaf size
      description:
        type: string
        const: Leaf size passed to BallTree or KDTree. This can affect the speed of
          the construction and query, as well as the memory required to store the
          tree.
      minOccurs:
        type: integer
        const: 0
      maxOccurs:
        type: integer
        const: 1
      schema:
        $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/schema.yaml#/properties/leaf_size
  output_column:
    type: object
    properties:
      title:
        type: string
        const: Output column name
      description:
        type: string
        const: Name of the column in which to store output metric. If this column
          exists, an error will be thrown
      minOccurs:
        type: integer
        const: 0
      maxOccurs:
        type: integer
        const: 1
      schema:
        $ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/schema.yaml#/properties/output_column

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputDescription/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputDescription/schema.yaml)


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
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputDescription/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/localoutlier/inputDescription`

