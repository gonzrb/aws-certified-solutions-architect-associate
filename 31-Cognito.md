1- What is Web identity Federation?

- Web Identity Federation lets you give your users access to AWS resources after they have successfully authenticated with a web-based identity provider like Amazon, Facebook, or Google. Following sucessful authentication, the user receives an authentication code from the Web ID provider, which they can trade for temporary AWS security credentials.

- Amazon Cognito provides Web Identity Federation with the following features:
    - Sign-up and sign-ip to your apps
    - Access for guest users
    - Acts as an Identity Broker between your application and Web ID providers, so you don't need to write any additional code.
    - Syncrhonizes user data for multiple devices.
    - Recommended for all mobile applications AWS services.

- Cognito prokers between the app and Facebook or Google to provide temporary credentials which map to an IAM role allowing acess to the required resources.
- No need for the application to embed or store AWS credentials locally on the device and it gives users a seamless experience across all mobile devices.

4- What is User Pool?

- User Pools are user directories use to manage Sing-ip and sign-in functionality for mobile and web applications.
- Users can sign-in directly to the User Pool, or using Facebook, Amazon or Google. Cognito acts as an Identity Broker between the identity provider and AWS. Successful authentication generates a JSON Web token (JWTs).

3- What is Identity Pool?

- Identity Pools provide temporary AWS credentials to access AWS services like S2 or DynamoDB.

4- Synchronisation

- Cognito tracks the association between user identify and the various different devices they sign-in from. In order to provide a seamless user experience for yoru application, Cognito uses Push Synchronization to push updates and synchronize user data across multiple devices. Cognito uses SNS to send a notification to all the devices associated with a given user identify whenever data stored in the cloud changes.
