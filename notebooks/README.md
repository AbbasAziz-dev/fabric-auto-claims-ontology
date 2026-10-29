# Fabric notebook plan

## `create_lakehouse_tables.ipynb`

Creates small demo Delta tables from approved sample data and verifies keys and foreign-key columns.

## `create_fabric_ontology.ipynb`

Reads `ontology/claims-fabric.yaml`, converts the approved profile to the Microsoft Fabric Ontology API payload, and creates or updates the Fabric ontology item.

The notebook must remain in Plan/preview mode until the Fabric API contract, workspace, Lakehouse, authentication, and preview feature availability are confirmed.

