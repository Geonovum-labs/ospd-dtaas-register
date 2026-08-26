
# Demo OGC API processes instance - LOF (Api)

`geonovum.dtaas.ogcapi.processes.custom-api` *v1.0*

An example of an OGC API Processes implementation using building blocks - Local Outlier Factor

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Localoutlier process description
A process description returned by the custom API.
#### json
```json
{
  "version": "0.1",
  "id": "localoutlier",
  "title": "Local outlier factor (LOF)",
  "description": "The local outlier factor (LOF) algorithm computes a score indicating the degree of abnormality of each input observation.",
  "keywords": ["local outlier factor", "LOF", "outlier detection"],
  "jobControlOptions": ["sync-execute", "async-execute"],
  "inputs": {
    "dataset": {
      "title": "Dataset",
      "description": "GeoJSON dataset of points in one CRS for which LOF scores should be computed.",
      "schema": {"type": "string", "format": "url"},
      "minOccurs": 1,
      "maxOccurs": 1
    },
    "n_neighbors": {
      "title": "Number of neighbors",
      "description": "Number of neighbors to use for neighbor queries.",
      "schema": {"type": "integer", "default": 20},
      "minOccurs": 0,
      "maxOccurs": 1
    },
    "leaf_size": {
      "title": "Leaf size",
      "description": "Leaf size passed to the spatial tree.",
      "schema": {"type": "integer", "default": 30},
      "minOccurs": 0,
      "maxOccurs": 1
    },
    "output_column": {
      "title": "Output column name",
      "description": "Name of the column in which to store the output metric.",
      "schema": {"type": "string", "default": "abnormality"},
      "minOccurs": 0,
      "maxOccurs": 1
    }
  },
  "outputs": {
    "output_dataset": {
      "title": "Output Dataset",
      "description": "The input dataset with the computed LOF metric.",
      "schema": {"type": "object", "contentMediaType": "application/json"}
    }
  },
  "outputTransmission": ["value"]
}
```


### Localoutlier execution request
A synchronous execution request for a GeoJSON point dataset.
#### json
```json
{
  "inputs": {
    "dataset": "https://example.org/data/points.geojson",
    "n_neighbors": 5,
    "leaf_size": 30,
    "output_column": "abnormality"
  }
}
```


### Localoutlier execution response
A synchronous execution response containing the processed dataset.
#### json
```json
{
  "outputs": {
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
}
```


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/custom-api`

