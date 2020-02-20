1- What is SWF?

- Amazon Simple Workflow Service (Amazon SWF) is a web service that makes it easy to coordinate work across distributed application components. SWF enables applications for a range of use cases, including media processing, web application back-ends, business process workflows, and analytics pipelines, to be designed as a condination of tasks.
- Task represent invocations of various processing steps in an application which can be performed by executable code, web service call, human action, and scripts.

2- SWF vs. SQS

- SQS has a retention period of up to 14 days: with SWF, workflow executions can last up to 1 year.
- Amazon SWF presents a task-orientated API, whereas Amazon SQS offers a message-oriented API
- Amazon SWF ensures that a task is assigned onyl once and is never duplicated. With Amazon SQS, you nee to handle duplicated messages and may also need to ensure that a message is processed only once.
- Amazon SWF keeps track of all the tasks and events in an application. With Amazon SQS, you need to implement your own application-level tracing, especially if your applciation uses multiple queues.

3- SWF Actors:
- Workflow Starters: An application that can intiate (start) a workflow. Could be your e-commerce website following the placement of an order, or a mobile app searching for bus times.
- Deciders: Control the flow of activity tasks in a workflow execution. If something has finished (or failed) in a workflow, a Decider decides what to do next.
- Activity Workers: Carry out the activity tasks.
