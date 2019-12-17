1- What is StorageGetaway?

- AWS Storage Getaway is a service that connects an on-premises software appliance with cloud-based storage to provide seamless and secure integration between an organization's on-premises IT environment and AWS's storage infrastructure. The service enables you to securely store data to the AWS cloud for scalable and cost-effective storage.

- AWS Storage Getaway's software appliance is available for download as a virtual machine (VM) image that you install on a host in your datacenter. Storage Getaway supports either VMvware ESXi or Microsoft Hyper-V. Once you have installed your getaway and associated it with your AWS account through the activation process, you can use the AWS MAnagement Console to create the storage getaway option that is right for you.

2- Four types of Storage Gateways

- File Getaway (NFS)
- Volumes Getaway (ISCSI)
    - Stored Volumes
    - Cached Volumes
- Tape Gateway (VTL)

3- File Getaway

- Files are stored as objects in your S3 buckets, accessed through a Network File System (NFS) mount point. Ownership, permissions, and timestamps are durably with the file. Once objects are transferred to S3, they can be managed as native S3 objects, and bucket policies such as versioning, lifecycle management, and cross-region replication apply directly to objects stored in your bucket.

4- Volume Gateway

- The volume interface presents your applications with disk volumes using the ISCSI block protocol.
- Data written to these volumes can be asynchronously backed up as point-in-time snapshots of your volumes, and stored in the cloud as Amazon EBS snapshots.
- Snapshots are incremental backups that capture only changed blocks. All snapshot storage is also compressed to minimize your storage charges.
- Three types:
    - Stored Volumes
        - Stored volumes let you store your primary data locally, while asynchronously backing up that data to AWS. Stored volumes provide your on-premises applications with low-latency access to their entire datasets, while providing durable, off-site bakups You can create storage volumes and mount them as iSCSI devices from your on-premises application servers. Data written to your stored volumes is stored on your on-premises storage hardware. This data is asynchronously backed yp to Amazon S3 in the form of Amazon Elastic Block Store (Amazon EBS) snapshots. 1GB-16TB in size for Stored Volumes.
    - Cached Volumes
        - Cached volumes let you use Amazon S3 as your primary data storage while retaining frequently accessed data locally in your storage getaway. Cached volumes minimize the need to scale your on-premises storage infrastructure, while still providing your applications with low-latency access to their frequently accessed data.
        - You can create storage volumes up to 32TiB in size and attach to them as iSCSI devices from your on-premises application servers. Your getaway stores data that you write to these volumes in Amazon S3 and retains recently read data in your on-premises storage getaway's cache and upload buffer storage. 1GB-32TB in size for Cached Volumes.
    - Tape Gateway
        - Tape Getaway offers a durable, cost-effective solution to archive your data in the AWS Cloud. The VTL interface it provides lets you leverage your existing tape-based backup application infrastructure to store data on virtual tape cartridges that you create on your tape gateway. Each tape gateway is available to your existing client backup applications as iSCSI devices. You add tape catridges as you need to archive your data. Supported by NetBacukp, Backup Exec, Veeam, etc.
