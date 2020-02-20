1- What is SNS?

- Amazon Simple Notification Service (Amazon SNS) is a web service that makes it easy to set up operate, and send notifications from the cloud. It provides developers with a highly scalable, flexible, and cost-effective capability to publish messages from an application and inmediately deliver them to subscribers or other applications.
- Push Notifications to Apple, Google, Fire OS and Windows devices, as well as Android devices in China with Baidu Cloud Push. Besides pushing cloud notifications directly to mobile devices, Amazon SNS can also deliver notifications by SMS tect message or email to Amazon Simple Queue Service (SQS) queues, or ty any HTTP endpoint.
- SNS allows you to group multiple recipients using topics. A topic is an "access point" for allowing recipients to dynamically subscribe for identical copiues of the same notifcation.
One topic can support deliveries to multiple endpoints types - for example, you can group together IOS, Android and SMS recipients. When you publish once to a topic, SNS delivers appropriately formatted copies of your message to each subscriber.
- To prevent messages from being lost, all messages published to Amazon SNS are stored redundantly across multiple availability zones.

2- Benefits:

- Instantaneous, push-based delivery (no polling)
- Simple APIs and easy tintegration with applications
- Flexible message delivery over multiple transport protocols
- Inexpensive, pay-as-you-go model with no up-front costs
- Web-based AWS Management Console offers the simplicity of a point-and-click interface

3- SNS vs. SQS

- Both Messaging Services in AWS
- SNS is push
- SQS Polls (pulls)