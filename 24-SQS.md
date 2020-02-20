1- What is SQS?

- Amazon SQS is a web service that gives you access to a message queue that can be used to store messages while waiting for a computer to process them. Amazon SQS is a distributed queue system that enables web service applications to quickly and reliably queue messages that one component in the application generats to be consumed by another component. A queue is a temporary repository for messages that are awaiting processing.
- Using Amazon SQS< you can decouple the components of an applciation so they run independently, easing message management between components. Any component of a distributed applciation cab store messages in a fail-safe queue. Messages can contain up to 256KB of text in any format. Any component can later retrieve the messages programmatically using the Amazon SQS API.

2- Types:
    - Standard: Amazon SQS offers standard as the default queue tpye. A standard lets you habve a nearly-unlimited number of transactions per second. Standard queues guarantee that a message is delivered at least once. However, occasionally (because of the highly-ditributed architecture that allows high thourghput), more than one copy of a message might be delivered out of order. Standard queues provide best-effort ordering which ensures that messages are generally delivered in the same as they are sent.
    - FIFO: The FIFO queue complements the standard queue. The most important features of this queue type are FIFO (first-in-first-out) delivery and exactly-once processing: The order in which messages are sent and received is stricly preserved and a message is delivered once and remains available until a consumer processes and deletes it: duplicates are not introduced into the queue. FIFO queues also support mesage groups that allow multiple ordered message groups within a single queue. FIFO queues are limited to 300 transactions per second (TPS), but have all the capabilities of standard queues.

- SQS is a way to de-couple your infrastructure.
- SQS is pull based, not pushed based.
- Messages are 250 KB in size.
- Messages can be kept in thr queue from 1 minute to 14 days; the default retention period is 4 days.
- Visibility Time Out is the amount of time that the message is invisible in the SQS queue after a reader picks up that message. Provided the job is processed before the visiblity time out expires, the message will then be deleted from the queue. IF the job is not processed within that time, the message will become viible again and another reader will process it. This could result in the same message being delivered twice.
- Visibility Time Out maximum is 12 hours.
- SQS guarantees that your message wil be processed at least once.
- Amazon SQS long polling is a way to retrieve messages from your Amazon SQS queues. While the regulat short polling returns inmediatelly (even if the message queue being polled is empty), long polling doesn't return a response until a message arrives in the message quee, or the long poll tiems out.
