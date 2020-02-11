1- What is Redshift?

- Amazon Redshift is a fast and powerful, fully managed, petabyte-scale data warehouse service in the cloud. Customers can start small for just $0.25 per hour with no commitments or upfront costs and scale to a petabyte or more for $1000 per terabyte per year, less than a tenth of most other data warehousing solutions. Used for business inteligence.

2- Redshift Configuration

- Redshift can be configured as follows:
	- Single Node (160GB)
	- Multi Node 
		- Leader Node (manages client connections and receives queties)
		- Compute Node (store data and perform queries and computations). Up to 128 Compute Nodes.

3- Advance Compression

- Columnar data stores can be compressed much more than row-based data stores because similar data is stored sequencially on disk. Amazon Redshift employs multiple compression techniques and can often achieve significant compression relative to traidicional relational data stores. In addition, Amazon Redshift doesn't require indexes or materialized views, and so uses less space than traditional relational database systems. When loading data into an empty table, Amazon Redshift automatically samples your data and selects the most appropiate compression schema. 

4- Backups

- Enabled by default with a 1 day retention period.
- Maximum retention period is 35 days.
- Redshift always attempt to mantain at least three copies of your data (the original and replica on the compute nodes and a backup in Amazon S3).
- Redshift can also asynchronously replicate your snapshots to S3 in another region for disaster recovery.

5- Pricing

- Compute Node Hours (total number of hours you run across all your compute nodes for the billing period. You are billed for 1 unit per node per hour, so a 3-node data warehouse cluster running persistently for an entire month would incur 2.160 instance hours. You will not be charged for leader node hours, only compute nodes will incur charges).

6- Security

- Encrypted in transit using SSl
- Encrypted at rest using AES-256 encryption 
- By default Redshift takes care of the key management.
	- Manage your own keys through HSM
	- AWS Key Management Service

7- Availability

- Currently only available in 1 AZ
- Can restore snapshots to new AZs in the event of an outage.