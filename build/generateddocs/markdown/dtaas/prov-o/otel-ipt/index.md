
# Local Outlier Factor OGC API Process with IPT provenance attributes from OpenTelemetry trace (Schema)

`geonovum.dtaas.prov-o.otel-ipt` *v0.1*

OTLP JSON trace transformed to IPT Provenenance from OGC API Processes.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Localoutlier OpenTelemetry trace mapped to IPT Profile
An OTLP JSON trace carrying the DTaaS processing activity, subject, and object attributes.
#### json
```json
{
  "description": "Example IPT provenance output for a Local Outlier Factor process after the OTLP-to-PROV mapping.",
  "process": {
    "id": "localoutlier_simple",
    "type": "https://example.org/processes/localoutlier_simple"
  },
  "provenance": {
    "activity": {
      "id": "https://algoritmes.overheid.nl/nl/algoritme/maaidata-provincie-noordholland/68294175",
      "type": "prov:Activity",
      "label": "LocalOutlierFactor"
    },
    "used": [
      {
        "id": "http://localhost:5000/collections/catalog/items/pygeoapi.process.localoutlier.LOFProcessor",
        "type": "prov:Entity",
        "role": "dataObject"
      },
      {
        "id": "2011",
        "type": "prov:Entity",
        "role": "input"
      },
      {
        "id": "203",
        "type": "prov:Entity",
        "role": "input"
      },
      {
        "id": "204",
        "type": "prov:Entity",
        "role": "input"
      }
    ],
    "wasAssociatedWith": {
      "id": "http://localhost:5000/processes/localoutlier_simple",
      "type": "prov:SoftwareAgent"
    }
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/prov-o/otel-ipt/context.jsonld",
  "description": "Example IPT provenance output for a Local Outlier Factor process after the OTLP-to-PROV mapping.",
  "process": {
    "id": "localoutlier_simple",
    "type": "https://example.org/processes/localoutlier_simple"
  },
  "provenance": {
    "activity": {
      "id": "https://algoritmes.overheid.nl/nl/algoritme/maaidata-provincie-noordholland/68294175",
      "type": "prov:Activity",
      "label": "LocalOutlierFactor"
    },
    "used": [
      {
        "id": "http://localhost:5000/collections/catalog/items/pygeoapi.process.localoutlier.LOFProcessor",
        "type": "prov:Entity",
        "role": "dataObject"
      },
      {
        "id": "2011",
        "type": "prov:Entity",
        "role": "input"
      },
      {
        "id": "203",
        "type": "prov:Entity",
        "role": "input"
      },
      {
        "id": "204",
        "type": "prov:Entity",
        "role": "input"
      }
    ],
    "wasAssociatedWith": {
      "id": "http://localhost:5000/processes/localoutlier_simple",
      "type": "prov:SoftwareAgent"
    }
  }
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix ns1: <https://example.org/terms/> .
@prefix prov: <http://www.w3.org/ns/prov#> .

<file:///github/workspace/2011> a prov:Entity ;
    prov:role "input" .

<file:///github/workspace/203> a prov:Entity ;
    prov:role "input" .

<file:///github/workspace/204> a prov:Entity ;
    prov:role "input" .

<file:///github/workspace/localoutlier_simple> a <https://example.org/processes/localoutlier_simple> .

<http://localhost:5000/collections/catalog/items/pygeoapi.process.localoutlier.LOFProcessor> a prov:Entity ;
    prov:role "dataObject" .

<http://localhost:5000/processes/localoutlier_simple> a prov:SoftwareAgent .

[] dcterms:description "Example IPT provenance output for a Local Outlier Factor process after the OTLP-to-PROV mapping." ;
    ns1:process <file:///github/workspace/localoutlier_simple> ;
    ns1:provenance [ prov:used <file:///github/workspace/2011>,
                <file:///github/workspace/203>,
                <file:///github/workspace/204>,
                <http://localhost:5000/collections/catalog/items/pygeoapi.process.localoutlier.LOFProcessor> ;
            prov:wasAssociatedWith <http://localhost:5000/processes/localoutlier_simple> ] .


```

## Schema

```yaml
type: object
required:
- process
- provenance
properties:
  process:
    type: object
    required:
    - id
    - type
    properties:
      id:
        type: string
        x-jsonld-id: '@id'
      type:
        type: string
        x-jsonld-id: '@type'
    x-jsonld-id: https://example.org/terms/process
  provenance:
    type: object
    required:
    - activity
    - used
    - wasAssociatedWith
    properties:
      activity:
        type: object
        required:
        - id
        - type
        - label
        properties:
          id:
            type: string
            x-jsonld-id: '@id'
          type:
            type: string
            x-jsonld-id: '@type'
          label:
            type: string
            x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
      used:
        type: array
        items:
          type: object
          required:
          - id
          - type
          - role
          properties:
            id:
              type: string
              x-jsonld-id: '@id'
            type:
              type: string
              x-jsonld-id: '@type'
            role:
              type: string
              x-jsonld-id: http://www.w3.org/ns/prov#role
        x-jsonld-id: http://www.w3.org/ns/prov#used
        x-jsonld-type: '@id'
      wasAssociatedWith:
        type: object
        required:
        - id
        - type
        properties:
          id:
            type: string
            x-jsonld-id: '@id'
          type:
            type: string
            x-jsonld-id: '@type'
        x-jsonld-id: http://www.w3.org/ns/prov#wasAssociatedWith
        x-jsonld-type: '@id'
    x-jsonld-id: https://example.org/terms/provenance
x-jsonld-extra-terms:
  description: http://purl.org/dc/terms/description
x-jsonld-prefixes:
  rdfs: http://www.w3.org/2000/01/rdf-schema#
  prov: http://www.w3.org/ns/prov#

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/prov-o/otel-ipt/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/prov-o/otel-ipt/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "description": "http://purl.org/dc/terms/description",
    "process": {
      "@context": {
        "id": "@id",
        "type": "@type"
      },
      "@id": "https://example.org/terms/process"
    },
    "provenance": {
      "@context": {
        "id": "@id",
        "type": "@type",
        "label": "rdfs:label",
        "used": {
          "@context": {
            "role": "prov:role"
          },
          "@id": "prov:used",
          "@type": "@id"
        },
        "wasAssociatedWith": {
          "@id": "prov:wasAssociatedWith",
          "@type": "@id"
        }
      },
      "@id": "https://example.org/terms/provenance"
    },
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "prov": "http://www.w3.org/ns/prov#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/prov-o/otel-ipt/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/prov-o/otel-ipt`

