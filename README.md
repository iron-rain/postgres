# IRON RAIN POSTGRES

## Options
Each component is an optional extra, by default a single instance stateful Postgres system will be provisioned.  

#### HA provided by [Zalando Patroni](https://github.com/zalando/patroni)
- High Availability Modes:
    - Active Cluster
        - Single cluster.
        - One primary instance with a minimum of two secondary instances.
    - Active Standby Cluster
        - Minimum two clusters.
        - One cluster with a primary instance and any number of scalable secondary instances.
        - Second cluster with a mimimum of one secondary instance.
    - Active Active Cluster
        - Provided by [Symmds](https://github.com/JumpMind/symmetric-ds)
        - Minimum two cluster.
        - One cluster with a primary instance and any number of scalable secondary instances.
        - Second cluster with a primary instance and any number of scalable secondary instances.

#### S3 WAL and Backup provided by [PgBackrest](https://github.com/pgbackrest/pgbackrest)
- Write Ahead Logs (WAL)
    - Ensures data integrity, changes are written to a store ahead of being written to the database.
- S3 Backup
    - Remote backup that allows for on-line restores if required. 

#### Administrator Interface provided by [pgAdmin](https://github.com/postgres/pgadmin4)
- Web based GUI for managing Postgres clusters and databases.

#### PostGIS provided by [PostGIS](https://github.com/postgis/postgis)
- Spatial and geographically enabled Postgres.

#### RESTful API provided by [Postgrest](https://github.com/PostgREST/postgrest)
- REST API for interacting with Postgres databases.