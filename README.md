# symmetricds-manager


## Replication Architecture Option

- `bi-directional` Information can be sent from parent to child bi-directionally. The router for each table has to be specified.
- `parent-child`No need for table-specific routing information.All data will be routed from parent to child
- `child-slave` The router direction for each table has to be specified

## 2-Tier replication architecture

- Each table is required to specify a routing direction.
- Channels trigger will be created for each table that requires initial load and the initial route direction has to be specified.
