
# Subsidence Analysis (Schema)

`geonovum.dtaas.ogcapi.processes.varidian.subsidence-analysis` *v0.1*

A registered geoprocessing activity type for performing settlement calculations for urban development using the Deltares Atlantis calculation module.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Deltares Atlantis - Subsidence Analysis
A registry entry conforming to the geoprocessing activity type.
#### json
```json
    {
      "id": "https://registry.playground.planspace.nl/processes/subsidence_subsidence",
      "type": "https://w3id.org/ogc/rim/activity-type/ActivityType",
      "objectIdentifier": "https://registry.playground.planspace.nl/processes/subsidence_subsidence",
      "itemClass": "https://w3id.org/ogc/rim/activity-type/activityTypeItemClass",
      "validityStatus": "valid",
      "publicationStatus": "published",
      "title": "Deltares Atlantis - Subsidence Analysis",
      "description": "Performs settlement calculations for urban development using the Deltares Atlantis calculation module.",
      "usedEntityType": "https://example.org/def/SurchargeArea",
      "generatedEntityType": "https://example.org/def/SubsidenceResult",
      "associatedAgentType": "http://www.w3.org/ns/prov#SoftwareAgent"
    }
```

#### jsonld
```jsonld
{
  "@context": "https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/varidian/subsidence-analysis/context.jsonld",
  "id": "https://registry.playground.planspace.nl/processes/subsidence_subsidence",
  "type": "https://w3id.org/ogc/rim/activity-type/ActivityType",
  "objectIdentifier": "https://registry.playground.planspace.nl/processes/subsidence_subsidence",
  "itemClass": "https://w3id.org/ogc/rim/activity-type/activityTypeItemClass",
  "validityStatus": "valid",
  "publicationStatus": "published",
  "title": "Deltares Atlantis - Subsidence Analysis",
  "description": "Performs settlement calculations for urban development using the Deltares Atlantis calculation module.",
  "usedEntityType": "https://example.org/def/SurchargeArea",
  "generatedEntityType": "https://example.org/def/SubsidenceResult",
  "associatedAgentType": "http://www.w3.org/ns/prov#SoftwareAgent"
}
```

#### ttl
```ttl
@prefix acttype: <https://w3id.org/ogc/rim/activity-type/> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix prov: <http://www.w3.org/ns/prov#> .
@prefix rim: <https://w3id.org/ogc/rim/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://registry.playground.planspace.nl/processes/subsidence_subsidence> a acttype:ActivityType ;
    dct:description "Performs settlement calculations for urban development using the Deltares Atlantis calculation module." ;
    dct:title "Deltares Atlantis - Subsidence Analysis" ;
    acttype:associatedAgentType prov:SoftwareAgent ;
    acttype:generatedEntityType <https://example.org/def/SubsidenceResult> ;
    acttype:usedEntityType <https://example.org/def/SurchargeArea> ;
    rim:itemClass acttype:activityTypeItemClass ;
    rim:objectIdentifier "https://registry.playground.planspace.nl/processes/subsidence_subsidence"^^xsd:anyURI ;
    rim:publicationStatus rim:published ;
    rim:validityStatus rim:valid .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
title: Subsidence Analysis Activity Type
description: 'A profile of the Geoprocessing Activity Type for subsidence analysis
  activities.

  '
allOf:
- $ref: https://geonovum-labs.github.io/activity-type-register/build/annotated/register/schemas/geoprocessing-activity-types-schema/schema.yaml
- type: object
  properties:
    type:
      const: https://w3id.org/ogc/rim/activity-type/ActivityType
    itemClass:
      const: https://w3id.org/ogc/rim/activity-type/activityTypeItemClass
    usedEntityType:
      const: https://example.org/def/SurchargeArea
    generatedEntityType:
      const: https://example.org/def/SubsidenceResult
    associatedAgentType:
      const: http://www.w3.org/ns/prov#SoftwareAgent
  required:
  - usedEntityType
  - generatedEntityType
  - associatedAgentType
x-bblocks-metadata:
  itemIdentifier: geonovum.dtaas.ogcapi.processes.varidian.subsidence-analysis
  register: https://geonovum-labs.github.io/ospd-dtaas-register/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-04'

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/varidian/subsidence-analysis/schema.json)
* JSON version: [schema.json](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/varidian/subsidence-analysis/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "Register": "rim:Register",
    "RegisterSystem": "rim:RegisterSystem",
    "RegisterSpecification": "rim:RegisterSpecification",
    "RegisterItemClass": "rim:RegisterItemClass",
    "RegisterItem": "rim:RegisterItem",
    "RegisterAction": "rim:RegisterAction",
    "Concept": "rim:Concept",
    "ConceptVersion": "rim:ConceptVersion",
    "ConceptSystem": "rim:ConceptSystem",
    "Commitment": "rim:Commitment",
    "Agent": "prov:Agent",
    "Organization": "prov:Organization",
    "Person": "prov:Person",
    "label": "rdfs:label",
    "prefLabel": "skos:prefLabel",
    "definition": "skos:definition",
    "inScheme": {
      "@id": "skos:inScheme",
      "@type": "@id"
    },
    "runsOn": {
      "@id": "rim:runsOn",
      "@type": "@id"
    },
    "hasSpecification": {
      "@id": "rim:hasSpecification",
      "@type": "@id"
    },
    "definesSubstantiveChange": "rim:definesSubstantiveChange",
    "registerOwner": {
      "@id": "rim:registerOwner",
      "@type": "@id"
    },
    "registerManager": {
      "@id": "rim:registerManager",
      "@type": "@id"
    },
    "controlBody": {
      "@id": "rim:controlBody",
      "@type": "@id"
    },
    "registerSystemManager": {
      "@id": "rim:registerSystemManager",
      "@type": "@id"
    },
    "registerUser": {
      "@id": "rim:registerUser",
      "@type": "@id"
    },
    "hasCommitment": {
      "@id": "rim:hasCommitment",
      "@type": "@id"
    },
    "commitmentCategory": {
      "@id": "rim:commitmentCategory",
      "@type": "@vocab"
    },
    "access": "rim:accessCommitment",
    "persistence": "rim:persistenceCommitment",
    "transparency": "rim:transparencyCommitment",
    "definedIn": {
      "@id": "rim:definedIn",
      "@type": "@id"
    },
    "validatedBy": {
      "@id": "rim:validatedBy",
      "@type": "@id"
    },
    "versionOf": {
      "@id": "rim:versionOf",
      "@type": "@id"
    },
    "version": "rim:version",
    "valid": "rim:valid",
    "invalid": "rim:invalid",
    "published": "rim:published",
    "unpublished": "rim:unpublished",
    "appliesTo": {
      "@id": "rim:appliesTo",
      "@type": "@id"
    },
    "proposer": {
      "@id": "rim:proposer",
      "@type": "@id"
    },
    "actionType": {
      "@id": "rim:actionType",
      "@type": "@vocab"
    },
    "addition": "rim:additionAction",
    "publish": "rim:publishAction",
    "unpublish": "rim:unpublishAction",
    "invalidation": "rim:invalidationAction",
    "supersession": "rim:supersessionAction",
    "redaction": "rim:redactionAction",
    "deletion": "rim:deletionAction",
    "changeClassification": {
      "@id": "rim:changeClassification",
      "@type": "@vocab"
    },
    "substantive": "rim:substantiveChange",
    "clarifying": "rim:clarifyingChange",
    "correctional": "rim:correctionalChange",
    "startedAtTime": {
      "@id": "prov:startedAtTime",
      "@type": "xsd:dateTime"
    },
    "endedAtTime": {
      "@id": "prov:endedAtTime",
      "@type": "xsd:dateTime"
    },
    "wasAssociatedWith": {
      "@id": "prov:wasAssociatedWith",
      "@type": "@id"
    },
    "id": "@id",
    "type": "@type",
    "objectIdentifier": {
      "@id": "rim:objectIdentifier",
      "@type": "xsd:anyURI"
    },
    "functionalIdentifier": {
      "@id": "rim:functionalIdentifier",
      "@type": "xsd:anyURI"
    },
    "itemClass": {
      "@id": "rim:itemClass",
      "@type": "@id"
    },
    "inRegister": {
      "@id": "rim:inRegister",
      "@type": "@id"
    },
    "realizes": {
      "@id": "rim:realizes",
      "@type": "@id"
    },
    "validityStatus": {
      "@id": "rim:validityStatus",
      "@type": "@vocab"
    },
    "publicationStatus": {
      "@id": "rim:publicationStatus",
      "@type": "@vocab"
    },
    "isRedacted": {
      "@id": "rim:isRedacted",
      "@type": "xsd:boolean"
    },
    "isDeleted": {
      "@id": "rim:isDeleted",
      "@type": "xsd:boolean"
    },
    "title": "dct:title",
    "description": "dct:description",
    "relatedItem": {
      "@id": "rim:relatedItem",
      "@type": "@id"
    },
    "supersededBy": {
      "@id": "rim:supersededBy",
      "@type": "@id"
    },
    "supersedes": {
      "@id": "rim:supersedes",
      "@type": "@id"
    },
    "hasAction": {
      "@id": "rim:hasAction",
      "@type": "@id"
    },
    "usedEntityType": {
      "@id": "rim:activity-type/usedEntityType",
      "@type": "@id"
    },
    "generatedEntityType": {
      "@id": "rim:activity-type/generatedEntityType",
      "@type": "@id"
    },
    "associatedAgentType": {
      "@id": "rim:activity-type/associatedAgentType",
      "@type": "@id"
    },
    "informedByActivityType": {
      "@id": "rim:activity-type/informedByActivityType",
      "@type": "@id"
    },
    "rim": "https://w3id.org/ogc/rim/",
    "prov": "http://www.w3.org/ns/prov#",
    "dct": "http://purl.org/dc/terms/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "owl": "http://www.w3.org/2002/07/owl#",
    "acttype": "rim:activity-type/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum-labs.github.io/ospd-dtaas-register/build/annotated/dtaas/ogcapi/processes/varidian/subsidence-analysis/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/ospd-dtaas-register](https://github.com/Geonovum-labs/ospd-dtaas-register)
* Path: `_sources/ogcapi/processes/varidian/subsidence-analysis`

