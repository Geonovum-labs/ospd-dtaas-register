
# Localoutlier process output schema (Schema)

`geonovum.dtaas.ogcapi.processes.schemas.localoutlier.outputSchema` *v1.0*

Output schema for the localoutlier process

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Localoutlier output values
#### json
```json
{
  "output_dataset": {
    "type": "FeatureCollection",
    "features": [
      {
        "type": "Feature",
        "properties": {"abnormality": 1.05},
        "geometry": {"type": "Point", "coordinates": [5.1214, 52.0907]}
      }
    ]
  }
}
```

## Schema

```yaml
type: object
properties:
  output_dataset:
    type: object
    contentMediaType: application/json

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputSchema/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/schemas/localoutlier/outputSchema/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/schemas/localoutlier/outputSchema`

