# ACORD Auto Claims Ontology for Microsoft Fabric

This project is a Fabric-oriented implementation of the ACORD-first Auto Claims Phase 0 ontology.

The canonical semantic source remains the W3C RDF/OWL/SKOS/SHACL package in:

`../ontology/auto-claims-phase0/`

This repository adds a readable YAML implementation specification for Microsoft Fabric entity types, properties, relationships, and data bindings. It does not replace the ACORD ontology.

## Architecture

```text
ACORD Information Model 2.7 + Data Model 2.7.2
                 |
                 v
Canonical OWL/RDF/SKOS/SHACL ontology
                 |
                 v
ACORD-to-Fabric YAML implementation profile
                 |
                 v
Microsoft Fabric Ontology entity types and relationships
                 |
                 v
Lakehouse tables and foreign-key bindings
```

## Repository layout

- `ontology/claims-fabric.yaml` — Fabric entity types, properties, relationships, and bindings.
- `ontology/acord-to-fabric.yaml` — provenance and crosswalk from ACORD IRIs to Fabric names.
- `data/README.md` — planned Phase 0 Lakehouse source tables.
- `notebooks/README.md` — planned Fabric notebook workflow.
- `visualization/README.md` — planned stakeholder graph view.

## Phase 0 scope

The initial model covers Loss Notification through Claim for Auto claims:

- Claim
- Loss Notification
- Loss Occurrence
- Financial Services Agreement
- Party
- Claim Declarer
- Party Role in Claim
- Vehicle
- Driver
- Place
- Peril
- Claim Status
- Communication Medium

Coverage, Exposure, Payment, Repair, Settlement, and detailed liability concepts remain deferred.

## Important modeling rule

ACORD terms and IRIs are canonical. Fabric names are implementation names and must retain an explicit `acord_iri` or mapping entry so that the Fabric model can be traced back to ACORD.

## Next implementation step

After the YAML profile is reviewed, create a Fabric notebook that reads the YAML and submits the corresponding Fabric Ontology definition through the supported Fabric API. Authentication, workspace identifiers, Lakehouse names, and Fabric preview capabilities must be supplied before that notebook can be executed.

