# Overview of Supply Chain Security Tools for Tanzu – Store

This topic gives you an overview of Supply Chain Security Tools (SCST) – Store.

SCST - Store stores the metadata generated by supplies chains in the Tanzu
Application Platform. It is made up of two services: Artifact Metadata
Repository (AMR) and Metadata Store.

## Artifact Metadata Repository

### <a id='observer'></a> AMR Observer

AMR Observer is a set of managed controllers that watches for relevant updates
on resources of interest. When relevant events are observed, a CloudEvent is
generated and sent to AMR CloudEvent Handler. This component is expected to be
deployed on Full, Build and Run profile clusters.

### <a id='handler'></a> AMR CloudEvent Handler

AMR CloudEvent Handler receives CloudEvents and stores relevant information into 
the Artifact Metadata Repository or Metadata Store. This component is expected
to be deployed on Full and View profile clusters.

### Additional Resources

- [AMR Architecture](amr/architecture.hbs.md)
- [AMR Configuration](amr/configuration.hbs.md)
- [AMR Data Models](amr/data-model-and-concepts.hbs.md)
- [AMR GraphQL Query](amr/graphql-query.hbs.md)

## Metadata Store

For more information about the Metadata Store, see
[Metadata Store overview](mds-overview.hbs.md).
