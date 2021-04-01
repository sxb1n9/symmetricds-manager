# symmetricds-manager
A SymmetricDS manager for easing the creation of node properties file and relivant SQL queries for instantiating SymmetricDS replications.

## Replication Architecture Options

- `bi-directional` Information can be sent from parent to child bi-directionally. The router for each table has to be specified.
- `parent-child`No need for table-specific routing information.All data will be routed from parent to child
- `child-slave` The router direction for each table has to be specified

### Bi-directional(2-Tier replication) Architecture

- Each table is required to specify a routing direction.
- Additional channel triggers will be created for each table that requires initial load thus requiring an initial route direction for the table in the JSON configuration file.
