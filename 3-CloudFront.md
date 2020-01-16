1- What is a CDN

- A content delivery network (CDN) is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage and a content delivery server.

- Edge Location: This is the location where content will be cached. This is separate to an AWS Region/AZ.
- Origin: This is the origin of all the files that the CDN will distribute This can be either an S3 bucket, an EC2 Instance, an Elastic Load Balancer or Route53.
- Distribution: This is the name given the CDN which consists of a collection of Edge Locations.
- Web Distribution: Typically used for Websites.
- RTMP: Userd for MEdia Streaming.

2- What is CloudFront

- Amazon CloudFront can be used to deliver your entire website, including dynamic, static, streaming, and interactive content using a global network of edge locations. Requests for your content are automatically routed to the nearest edge location, so cotnetn is delivered with the best possible performance.
- Amazon CloudFront is optimized to work with other Amazon Web Services, like Amazon simple Storage, Service (Amazon S3), Amazon Elastic Load Compute Cloud (Amazon EC2), Amazon Elastic Load Balancing, and Amazon Route 53. Amazon CloudFront also works seamlessly with any non-AWS origin server, which stores the original, definitive versions of your files.

- Edge locations are not jusy READ only, you can write to them too (ie out an object on to them).
- Objects are cached for the life of the TTL (Time to live)
- You can clear cached objects, but you will be charged.
