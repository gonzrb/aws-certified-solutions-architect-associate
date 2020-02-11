1- What is Aurora?

- Amazon Aurora is a MySQL and PostgreSQL-compatible relational database engine that combines the speed and availability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora provides up to five times better performance than MySQL and three times better than PostgreSQL databases at a much lower price point, whislst delivering similar performance and availability.

2- Things to know:

- Start with 10GB, Scales in 10GB increments to 64TB (Storage Autoscaling).
- Compute resources can scale up to 32vCPUs and 244GB of Memory.
- 2 copies of your data is contained in each availability zone, with minimum of 3 availability zones, 6 copies of your data.

3- Scaling:

- Aurora is designed to transparently handle the loss of up to two copies of data without affecting database write availability and up to three copies without affecting read availability.
- Autora storage is also self-healing. Data blocks and disks are continuously scanned for errors and repaired automatically.

4- Replicas:

- Aurora Replicas (currently 15)
- MySQL Read Replicas (currently 5)

