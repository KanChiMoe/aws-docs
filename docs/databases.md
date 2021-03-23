
# RDS

Think database + EC2.

Can use SQL (like MySQL, PostgresSQL, Oracle, Microsoft SQL server).

Comes with automatic patching, backups, redundency, failover, and disaster recovery.

# Aurora 

Amazon's own type of database. It's **not** MySQL or Postgres, but it quacks like it.

Data is replicated across AZs(?) with 6 copies. 15 read replicas. Continus backups to S3. Point-in-time recovery.


# DynamoDB

Key-value DB. Think back to the mIRC tables, these are exactly the same. 

Also serverless.

# Redshift

Data warehousing/big data. Not serverless.

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

In memory database.

# DAX

Caching for DynamoDB.