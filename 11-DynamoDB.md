-1 What is DynamoDB?

- Amazon DynamoDB is a fast and flexible NoSQL database service for all applications that need consistent, single-digit milisecond latency at any scale. It is a fully managed database and support both document and key-value data models. Its flexible data model and reliable performance make it a great fit for mobile, web, gaming, ad-tech, ioT, and many other applications. 

2- The basics of DynamoDB

- Stored on SSD storage
- Spread across 3 geographically distinct data centers
- Eventual Consistent Reads (Defaults)
- Strongly Consistent Reads

3- Eventual Consistent Reads

- Consistency across all copies of data usually reached within a second. Repeating a read after a short time should return the updated data. (Best Read Performance)

4- Strongly Consistent Reads

- A strongly consistent read returns a result that reflects all writes that received a succesful response prior to the read.

\