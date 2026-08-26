
# OpenTelemetry trace with DTaaS provenance attributes (Schema)

`geonovum.dtaas.opentelemetry.trace` *v0.1*

OTLP JSON trace shape used to record OGC API Processes provenance.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Localoutlier OpenTelemetry trace
An OTLP JSON trace carrying the DTaaS processing activity, subject, and object attributes.
#### json
```json
{
  "resourceSpans": [
    {
      "resource": {
        "attributes": [
          {"key": "service.name", "value": {"stringValue": "localoutlier-api"}}
        ]
      },
      "scopeSpans": [
        {
          "scope": {"name": "geonovum.dtaas.localoutlier"},
          "spans": [
            {
              "traceId": "98bdcae79e7fa7d4ccbc981e0653e8fd",
              "spanId": "dff0fb279813ee0d",
              "parentSpanId": "",
              "name": "localoutlier.execute",
              "kind": 1,
              "startTimeUnixNano": "1739370701786437325",
              "endTimeUnixNano": "1739370702000265566",
              "attributes": [
                {"key": "ogc.process.id", "value": {"stringValue": "localoutlier"}},
                {"key": "dpl.core.processing_activity_id", "value": {"stringValue": "geonovum.dtaas.ogcapi.processes.custom-api/localoutlier"}},
                {"key": "dpl.core.data_subject_id", "value": {"stringValue": "demo-subject"}},
                {"key": "dpl.objects.data_object_id", "value": {"intValue": "2069296"}},
                {"key": "dpl.objects.data_object_def", "value": {"stringValue": "https://example.org/objects/point-dataset"}}
              ],
              "status": {"code": 1}
            }
          ]
        }
      ]
    }
  ]
}
```

## Schema

```yaml
type: object
required:
- resourceSpans
properties:
  resourceSpans:
    type: array
    items:
      type: object
      required:
      - resource
      - scopeSpans
      properties:
        resource:
          type: object
          properties:
            attributes:
              type: array
              items:
                $ref: '#/$defs/attribute'
        scopeSpans:
          type: array
          items:
            type: object
            required:
            - spans
            properties:
              scope:
                type: object
              spans:
                type: array
                items:
                  type: object
                  required:
                  - traceId
                  - spanId
                  - name
                  - startTimeUnixNano
                  - endTimeUnixNano
                  properties:
                    traceId:
                      type: string
                    spanId:
                      type: string
                    parentSpanId:
                      type: string
                    name:
                      type: string
                    kind:
                      type: integer
                    startTimeUnixNano:
                      type: string
                    endTimeUnixNano:
                      type: string
                    attributes:
                      type: array
                      items:
                        $ref: '#/$defs/attribute'
                    status:
                      type: object
                      properties:
                        code:
                          type: integer
$defs:
  attribute:
    type: object
    required:
    - key
    - value
    properties:
      key:
        type: string
      value:
        type: object
        properties:
          stringValue:
            type: string
          intValue:
            type: string
          boolValue:
            type: boolean

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/opentelemetry/trace/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/opentelemetry/trace/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/opentelemetry/trace`

