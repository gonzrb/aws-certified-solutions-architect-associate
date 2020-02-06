1- What is a RDS?

- Relational databases are what most of us are all used to. They have been around since the 70's. Think of a tradicional spreadsheet:
    - Database
    - Tables
    - Rows
    - Fields

- Options:
    - Amazon Aurora
    - SQL Server
    - Oracle
    - MySQL Server
    - PostgreSQL
    - MariaDB

- EDS has two key features:
    - Multi-AZ - For Disater Recovery
    - Read Replicas - For Performance

- Non Relational Databases are as follows:
    - Collection
    - Document
    - Key/Value Pairs

- Options:
    - Amazon's NRD DynamoDB

4- What is Data Warehousing?

- USed for businesss intelligence. Tools like Cognos, Jaspersoft, SQL Server Reporting Services, Oracle, Hyperion, SAP Netweaver.
- Used to pull in very large and complex data sets. Usually used by management to do queries on data (such as current performance vs. targets etc)

5- OLTP vs. OLAP

- Online Transaction Processing (OLTP) differs from OLAP Online Analytics Processing (OLAP) in terms of the type of queries you will run.
- Data Warehousing databases use different type of architecture bot hfrom a database perspective and infrastructure layer. 

- Options:
    - Redshift

6- ElastiCache

- ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory cache in the cloud. The service improves the performance of web applciations by allowing you to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slow disk-based databases.

- ElastiCache supports two open-source in-memory caching engines:
- Memcached
- Redis

- RDS runs on virtual machines
- You cannot log in to these operating systems however.
- Patching of the RDS Operating System and DB is Amazon's responsibility
- RDS is NOT Serverless
- Aurora Serverless IS Serverless

7- Automated Backups

- Automated Backups allow you to recover your database to any point in time within a "retention period". The retention period can be netween one and 35 days. Automated Backups will take a full daily snapshot and will also store transaction logs throughout the day. When you do a recovery, AWS will first choose the most recent daily back up, and then apply transaction logs relevant to that day. This allows you to do a point in time recovery down to a seconds, within the retention period.
- Automated Backups are enabled by default. The backup data is stored in S3 and you get free storage space equal to the size of you database. So fi you have an EDS instance of 10Gb, you will get 10Gb worth of storage.
- Backups are taken within defined window. During the backup window, storage I/O may be suspended while your data is being backed up and you may experience elevated latency.
- DB Snapshots are done manually (ie they are used initiated). They are stored even after you delete the original RDS instance, unlike automated backups.

8- Restoring Backups

- Whenever you restore either an Automatic Backup or a manual Snapshot, the restored version of the database will be a new RDS instance with a new DNS endpoint.
- Encryption at rest is supported for MySQL, Oracle, SQL Server, PostgreSQL, MariaDB & Aurora. Encryption is done using the AWS Key Management Service (KMS) service. Once your RDS instance is encrypted, the data stored at rest in the underlying storage is encrypted, as are its automated backups, read replicas, and snapshots.

9- What is Multi-AZ

- Multi-AZ allows you to have an exact copy of your production database in another Availability Zone. AWS handles the replication for you, so when your production database is written to, this write will automatically be synchronized to the stand by database.
- In the event of planned database mantenance, DB Instance failure, or an Availability Zone failure, Amazon EDS will automatically failover to the standby so that database operations can resume quickly without administrative intervention.

- Multi-AZ is available for the following databases:
    - SQL Server
    - Oracle
    - MySQL Server
    - PostgreSQL
    - MariaDB

10- What is a Read Replica

- Read replicas allow you to have a read-only copy of your production database. This is achieved by using Asynchronous replication from the primary RDS instance to the read replica. You use read replicas primarily for very read-heavy database workloads.


