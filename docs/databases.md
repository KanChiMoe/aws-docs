
# RDS

Relational databases. Uses SQL (like MySQL, PostgresSQL, Oracle, Microsoft SQL server).

Comes with automatic patching, backups, redundency, failover, and disaster recovery.

# Aurora 

Managed relational databases for MySQL or PostgresSQL.

Data is replicated across AZs(?) with 6 copies. 15 read replicas. Continus backups to S3. Point-in-time recovery.

!!! danger "Review this"
    The above two seem to be the same. My understanding is that RDS is the whole shebang (optomised OS, Database) but Aurora is *just* the database? These two seem mostly the same as I'm not really noticing a difference between them.

    Addationally, the training doesn't cover if these are serverless or not. I assume you do.

# DynamoDB

Key-value DB. Think back to the mIRC tables, these are exactly the same. 

Also serverless.

# Redshift

Data warehousing/big data.

# Database Migration Service (DMS)

Move database (sql or not) to AWS. 

### Usecases

* Development and test migration - You can use DMS to make a copy of production data to dev enviorment to test against without affecting prod.
* Consolidation - merge several databases into one.
* Continuous replication - send ongoing copies to other targets.

## Homogenous

Source and target are the same type.

* MySQL, Microsoft SQL to EC2 or RDS

## Hetrogenous 

Source and target are of different types.

* Need to be converted using the conversion tool. Will change the schema and code to match target.
* Use DMS to target.

# DocumentDB

Think content management system.

# Neptune

Graphing database. Who is connected to who kind. For social networking and recomendations and fraud detection.

# QLDB

Think financial actions tracking. Any entry can never be removed.

# Managed Blockchain

For blockchains.

# ElastiCache

Caching ontop of databases.

# DAX

Caching for DynamoDB.