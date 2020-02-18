1- What is API Gateway?

- Amazon API Gateway is a fully managed service that makes it easy for developers to publish, maintain, monitor, and secure APIs at any scale.
- With a few clicks in the AWS Management Console, you can create an API that acts as a "front door" for applications to acces data, business logic, or functionality from your back-end services, such as applications runnign on Amazon Elasti Compute Cloud (Amazon EC2), code running on AWS Lambda, or any web applciation.

2- What can API Gateway do?

- Expose HTTPS endpoints ot define RESTful API
- Serverless-ly connect to services like Lambda & DynamoDB
- Send each API endpoint to a different target
- Run efficiently with low cost
- Scale effortlessly
- Track and control usage by API key
- Throuttle requests to preent attacks
- Connect to CloudWatch to log all request for monitoring
- Mantain multiple versions fo your API

3- How do I configure API Gateway?

- Define an API (container)
- Define Resources adn nested Resources (URL paths)
- For each Resource:
    - Select supported HTTP methods (verbs)
    - Set security
    - Choose target (such as EC2, Lambda, DynamoDB, etc)
    - Set request and response transformations

4- How do i deploy API Gateway?

- Deploy API to a stage:
    - Uses API Gateway domain, by default
    - Can use custom domain
    - Now supports AWS Certificate Manager: free SSl/TLS certs

- You can enalbe API caching in AMazon API Gateway to cache your enpoint's response. With caching, you can reduce the nbumber of calls made to your endpoint and also improve the lateny of the requests to your API. When you enable caching for a stage, API Gateway caches responses form your endpoint for a specified time-to-live (TTL) perriod, in seconds. API Gateway then responds to the request by looing up the endpoint response from the cache instead of making a request to your endpoint.
- IN computing, the same-origin policy is an important concept in the web application security model. Uder the policy, a web browser permits scripts contained in a fisert web page to access data in a second web page, but only if both web pages have the same origin.
- This is done to prevent Cross-Site Scripting (XSS) attacks.
    - Enforced by web browsers
    - Ignored by tools like PostMan and curl
- CORS is one way the server at the other end (not the client code in the browser) can relax the same-origin policy.
- Cross-origin resource sharing (CORS)is a mechanism that allowsd restricted resources (e.g. fonts) on a web page to be requested from another domain outside the domain from which the first resource was served.
