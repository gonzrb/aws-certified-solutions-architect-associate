1- What is Lambda?

- Lambda is The Ultimate Abstraction Layer:
    - Data Centers
    - hardware
    - Assembly Code/Protocols
    - High Level Languages
    - Operating Systems
    - Application Layer/AWS APIs
    - AWS lambda

- AWS LAmbda is a compute service where you can upload your code and create lambda function. AWS Lambda takes care of provisioning and managing the servers that you use to run the code. You don't have to worry about operating systems patching, scalling, etc.
- You can use Lambda in the following ways:
    - As an event-driven compute service where AWS Lambda runs your code in response to events. There events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table.
    - As a compute service to run your code in response to HTTP requests using Amazon API Gateways or API calls made using AWS SDKs.

2- What languages does lambda support?

- NodeJS
- Java
- Python
- C#
- Go
- PowerShell

3- How is Lambda priced

- Number of requests: First 1 millon requests are free. $0.20 per 1 millon requests thereafter.
- Duration: Duration is calculated from the time your code begins executing until it returns or otherwise terminates, rounded up to the nearest 100ms. The price depends on the amount of memory you allocate to your function. You are charged $0.000001667 for every GB second used.

4- Why is Lambda cool?

- No servers.
- Continuos Scaling.
- Super cheap.

- Lambda scales out (not up) automatically.
- Lambda functions are independent, 1 event = 1 function.
- Lambda is serverless.
- Aurora Serverless is the only other service that is serverless.
- Lambda functions can trigger other lambda functions, 1 event can = x functions if functions trigger other functions.
- Architecture can get extremely complicated, AWS X-ray allows you to debug what is happening.
- Lambda can do trings globally, you can use it to back up S3 buckets to other S3 buckets etc.
