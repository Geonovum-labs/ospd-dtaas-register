
# IPT profile of Geonovum custom API processes (Api)

`geonovum.dtaas.ogcapi.processes.custom-api-ipt` *v0.1*

Profile of Geonovum's custom OGC API Processes for IPT (Integrity Provenance Trust) aspects.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### IPT provenance-bearing process result
A custom API result using the OGC IPT results schema with a PROV activity inline.
#### json
```json
{
  "encoding": "json",
  "mediaType": "application/ld+json",
  "schema": "https://example.org/provenance/activity/98bdcae79e7fa7d4ccbc981e0653e8fd",
  "value": {
    "id": "https://example.org/provenance/activity/98bdcae79e7fa7d4ccbc981e0653e8fd",
    "provType": "Activity",
    "startedAtTime": "2025-02-12T10:31:41.786437325Z",
    "endedAtTime": "2025-02-12T10:31:42.000265566Z",
    "used": "https://example.org/objects/point-dataset",
    "wasAssociatedWith": "https://example.org/provenance/agent/geonovum.dtaas.ogcapi.processes.custom-api/localoutlier",
    "qualifiedUsage": {
      "id": "https://example.org/provenance/usage/2069296",
      "type": "Usage",
      "entity": "https://example.org/objects/point-dataset"
    }
  }
}
```


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/custom-api-ipt`

