1- What is a Load Balancer?

- A load balancer is a phisical or virtual device designed to help balance the load across multiple servers.

- Types:
	- Applicantion Load Balancer: Best suited for load balancing of HTTP and HTTPS traffic. They operate at Layer 7 and are application-aware. They are inteligent, and you can rreate advanced request routing, sending specified request to specific web servers.
	- Network Load Balancer: Best suited for load balancing TCP traffict where extreme performance is required. Operating at the connection level (Layer 4), Network Load Balancer are capable of handling millons of requests per second, while maintaining ultra-low latencies.
	- Classic Load Balancer: are the legacy Elastic Load Balancers. You can load balance HTTP/HTTPS applications and use Layer 7-specific features, such as X-Fowarded and sticky sessions. You can also use strict Layer 4 load balancing for applications that rely purely on the TPC protocol.

- 504 Error means gateway has timed out. This means that the application is not responding within the idle timeout period.
- Trouble shoot the application. Is the Web Server or Database Server?
- IF you need IPv4 address of your end user, look for the X-Forwared-For header.
- Instance monitored by ELB are reported as: InService, or OutofService.
- Health Checks check the instance health by talking to it.
- Load Balancers have their own DNS name. You are never given an IP address.

2- Advanced Load Balancers

- Sicky Sessions: enable you users to stick to the same EC2 instace. Can be useful if you are storing information locally to that instance.
- Cross Zone Load Balancing: Enables yo ut ocross balance across multiple availability zones.
- Path Patterns: allow you to direct traffict to different EC2 instances based on the URL contained in the request.
