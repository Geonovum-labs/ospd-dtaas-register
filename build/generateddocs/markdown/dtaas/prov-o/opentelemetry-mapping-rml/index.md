
# OpenTelemetry to PROV-O mapping (RML plugin) (Schema)

`geonovum.dtaas.prov-o.opentelemetry-mapping-rml` *v0.1*

OpenTelemetry OTLP JSON transformed to PROV-O RDF using an RML transform plugin.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Mapping from OpenTelemetry (LDV profile) to PROV-O (RML based)

This building block performs the transform from Opentelemetry to PROV-O using a (experimental) RML Transformer.


## Examples

### OTLP to PROV-O RML transform input
An OTLP trace transformed into PROV-O RDF using the RML plugin.
#### json
```json
{
    "resourceSpans": [
        {
            "resource": {
                "attributes": [
                    {
                        "key": "service.name",
                        "value": {
                            "stringValue": "http://localhost:5000/processes/localoutlier_simple"
                        }
                    }
                ]
            },
            "scopeSpans": [
                {
                    "scope": {
                        "name": "localoutlier_simple.tracer"
                    },
                    "spans": [
                        {
                            "traceId": "14e2af11847bde8d76f65f7c6e8d86e0",
                            "spanId": "f2773d02c278c008",
                            "parentSpanId": "",
                            "flags": 256,
                            "name": "LocalOutlierFactor",
                            "kind": 1,
                            "startTimeUnixNano": "1787910165430949248",
                            "endTimeUnixNano": "1787910165607410083",
                            "attributes": [
                                {
                                    "key": "dpl.objects.processing_activity_id",
                                    "value": {
                                        "stringValue": "https://algoritmes.overheid.nl/nl/algoritme/maaidata-provincie-noordholland/68294175"
                                    }
                                },
                                {
                                    "key": "dpl.objects.dataproduct_id",
                                    "value": {
                                        "stringValue": "http://localhost:5000/collections/catalog/items/pygeoapi.process.localoutlier.LOFProcessor"
                                    }
                                },
                                {
                                    "key": "dpl.objects.data_object_id",
                                    "value": {
                                        "arrayValue": {
                                            "values": [
                                                {
                                                    "intValue": "2011"
                                                },
                                                {
                                                    "intValue": "203"
                                                },
                                                {
                                                    "intValue": "204"
                                                },
                                                {
                                                    "intValue": "205"
                                                },
                                                {
                                                    "intValue": "206"
                                                },
                                                {
                                                    "intValue": "207"
                                                },
                                                {
                                                    "intValue": "208"
                                                },
                                                {
                                                    "intValue": "209"
                                                },
                                                {
                                                    "intValue": "210"
                                                },
                                                {
                                                    "intValue": "211"
                                                },
                                                {
                                                    "intValue": "212"
                                                },
                                                {
                                                    "intValue": "213"
                                                },
                                                {
                                                    "intValue": "214"
                                                },
                                                {
                                                    "intValue": "215"
                                                },
                                                {
                                                    "intValue": "216"
                                                },
                                                {
                                                    "intValue": "218"
                                                },
                                                {
                                                    "intValue": "225"
                                                },
                                                {
                                                    "intValue": "229"
                                                },
                                                {
                                                    "intValue": "233"
                                                },
                                                {
                                                    "intValue": "235"
                                                },
                                                {
                                                    "intValue": "236"
                                                },
                                                {
                                                    "intValue": "237"
                                                },
                                                {
                                                    "intValue": "238"
                                                },
                                                {
                                                    "intValue": "239"
                                                },
                                                {
                                                    "intValue": "240"
                                                },
                                                {
                                                    "intValue": "242"
                                                },
                                                {
                                                    "intValue": "248"
                                                },
                                                {
                                                    "intValue": "249"
                                                },
                                                {
                                                    "intValue": "251"
                                                },
                                                {
                                                    "intValue": "252"
                                                },
                                                {
                                                    "intValue": "257"
                                                },
                                                {
                                                    "intValue": "258"
                                                },
                                                {
                                                    "intValue": "260"
                                                },
                                                {
                                                    "intValue": "265"
                                                },
                                                {
                                                    "intValue": "267"
                                                },
                                                {
                                                    "intValue": "269"
                                                },
                                                {
                                                    "intValue": "270"
                                                },
                                                {
                                                    "intValue": "273"
                                                },
                                                {
                                                    "intValue": "275"
                                                },
                                                {
                                                    "intValue": "277"
                                                },
                                                {
                                                    "intValue": "278"
                                                },
                                                {
                                                    "intValue": "279"
                                                },
                                                {
                                                    "intValue": "280"
                                                },
                                                {
                                                    "intValue": "283"
                                                },
                                                {
                                                    "intValue": "285"
                                                },
                                                {
                                                    "intValue": "286"
                                                },
                                                {
                                                    "intValue": "290"
                                                },
                                                {
                                                    "intValue": "308"
                                                },
                                                {
                                                    "intValue": "310"
                                                },
                                                {
                                                    "intValue": "311"
                                                },
                                                {
                                                    "intValue": "312"
                                                },
                                                {
                                                    "intValue": "313"
                                                },
                                                {
                                                    "intValue": "315"
                                                },
                                                {
                                                    "intValue": "316"
                                                },
                                                {
                                                    "intValue": "317"
                                                },
                                                {
                                                    "intValue": "319"
                                                },
                                                {
                                                    "intValue": "320"
                                                },
                                                {
                                                    "intValue": "321"
                                                },
                                                {
                                                    "intValue": "323"
                                                },
                                                {
                                                    "intValue": "324"
                                                },
                                                {
                                                    "intValue": "330"
                                                },
                                                {
                                                    "intValue": "331"
                                                },
                                                {
                                                    "intValue": "340"
                                                },
                                                {
                                                    "intValue": "343"
                                                },
                                                {
                                                    "intValue": "344"
                                                },
                                                {
                                                    "intValue": "348"
                                                },
                                                {
                                                    "intValue": "350"
                                                },
                                                {
                                                    "intValue": "356"
                                                },
                                                {
                                                    "intValue": "370"
                                                },
                                                {
                                                    "intValue": "375"
                                                },
                                                {
                                                    "intValue": "377"
                                                },
                                                {
                                                    "intValue": "380"
                                                },
                                                {
                                                    "intValue": "391"
                                                },
                                                {
                                                    "intValue": "392"
                                                },
                                                {
                                                    "intValue": "871"
                                                },
                                                {
                                                    "intValue": "873"
                                                },
                                                {
                                                    "intValue": "990"
                                                }
                                            ]
                                        }
                                    }
                                },
                                {
                                    "key": "dpl.objects.dataset_id",
                                    "value": {
                                        "stringValue": "http://localhost:5000/collections/knmi_meetstations/queryables?f=json"
                                    }
                                }
                            ],
                            "status": {
                                "code": 1
                            }
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
$ref: https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/opentelemetry/trace/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/prov-o/opentelemetry-mapping-rml/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/prov-o/opentelemetry-mapping-rml/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/prov-o/opentelemetry-mapping-rml`

