# symmetricds-manager

A manager for easing the creation of node properties file and relivant SQL queries for instantiating SymmetricDS replications.

## Replication Architecture Options

- `bi-directional` This architecture allows information to flow in both directions between nodes. For example, specific data can be shared between a Headquarter and multiple branches in all direction. This architecture can still be used to replicate functionality of a parent-child or child-parent architecture. A router has to be specified for each table in the manager's JSON configuration file. See configuration section below for more details.

- `parent-child` Allows repliaction of data in one direction from parent to children only. No need for table-specific routing information.All data will be routed from parent to child
- `child-parent` Allows repliaction of data in one direction from children to parent only.The router direction for each table has to be specified

### Bi-directional (2-Tier replication) Architecture

- Each table is required to specify a routing direction since the replication of table could be from either parent to child or vice versa.
- Additional channel triggers will be created for each table that requires initial load thus requiring an initial route direction for the table in the JSON configuration file.

## Configuration

sample [JSON](https://www.json.org/json-en.html) configuration [file](sample/cnf.json) is included in the samples directory.
