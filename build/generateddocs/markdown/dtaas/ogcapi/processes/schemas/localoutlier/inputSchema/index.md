
# Localoutlier process input schema (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.localoutlier.inputSchema` *v1.0*

Input schema for the localoutlier process

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Localoutlier input values
#### json
```json
{
  "dataset": "https://example.org/data/points.geojson",
  "n_neighbors": 5,
  "leaf_size": 30,
  "output_column": "abnormality"
}
```

#### jsonld
```jsonld
{
  "@context": "https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/context.jsonld",
  "dataset": "https://example.org/data/points.geojson",
  "n_neighbors": 5,
  "leaf_size": 30,
  "output_column": "abnormality"
}
```

#### ttl
```ttl
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

[] xsd:integer 5,
        30 .


```

## Schema

```yaml
type: object
required:
- dataset
properties:
  dataset:
    type: string
    format: url
  n_neighbors:
    oneOf:
    - type: integer
    default: 20
    x-jsonld-id: http://www.w3.org/2001/XMLSchema#integer
  leaf_size:
    oneOf:
    - type: integer
    default: 30
    x-jsonld-id: http://www.w3.org/2001/XMLSchema#integer
  output_column:
    oneOf:
    - type: string
    default: abnormality

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "n_neighbors": "http://www.w3.org/2001/XMLSchema#integer",
    "leaf_size": "http://www.w3.org/2001/XMLSchema#integer",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/inputSchema/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/localoutlier/inputSchema`

