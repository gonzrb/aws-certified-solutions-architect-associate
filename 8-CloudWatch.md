1- What is CloudWatch?

- Amazon CloudWatch is a monitoring service to monitor your AWS resources, as well as the applications that you run on AWS.

2- What can CloudWatch monitor?

- CloudWatch can monitor things like
    - Compute
        - EC2 Instances
        - AUtoscaling Groups
        - Elastic Load Balancers
        - Route53 Health Checks
    - Storage & Content Delivery
        - EBS VOlumes
        - Storage Getaways
        - CloudFront

- What can I do with CloudWatch?

- Dashboards - Creates awesome dashboards to see what is happening with your AWS environment
- Alarms - Allows you to set Alarms that notify you when particular thresholds are hit.
- Events - CloudWatch Events helps you to respond to state changes in your AWS resources
- Logs - CloudWatch LOgs helps you to aggregate, monitor and store logs.

- CloudWatch & EC2

- Host Level MEtrics Consist of:
    - CPU
    - Network
    - Disk
    - Status Check

- What is AWS Cloud Trail?

- AWS CloudTrail increases visibility into your user and resource activity by recording AWS Management Console actions and API calls. You can identify which users and account called AWS, the source IP address from which the calls were made, and when the calls occurred.

- CloudTrail vs. CloudWatch

- CloudWatch monitors performance
- CloudWatch can monitor most of AWS as well as applications that run on AWS.
- CloudWatch with EC2 will monitor events every 5 minutes by default
- You can have 1 minute intervals by turning on detailed monitoring
- You can create CloudWatch alarms which trigger notifications
- CloudTrail monitors API calls in the AWS platform
- CouldWatch is all about performance. CloudTrail is all about auditing.
