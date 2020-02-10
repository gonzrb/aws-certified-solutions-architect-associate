

1-What is DNS?

- DNS is ussed to convert human friendly domain names into an Internet Protocol (IP) address. IP addresses are used by computers to identify each other on the network. IP addresses commonly come in 2 different forms, IPv4 and IPv6.

- ELBs do not have pre-defined IPv4 addresses: you resolve to them using a DNS name.

- DNS types:
    - SOA Records
    - NS Records
    - A Records
    - CNAMES
    - MX Records
    - PTR Records

- IPv4 vs. IPv6

- IPv4 ispace is a 32bit field and has over 4 billon different addresses.
- IPv6 was created to solve this depletion issue and has an address space of 128bits which in thery is340 undecilion addresses.

2- Top Level Domains

- If we look at common doman names such as google.com, bbcco.uk, acloud.guru, etc, you will notice a string of cahracters separated by dots (periods). The last word in a domain name represents the "top level domain". The second word in a domain name is known as a second level domai nname (this is optional though and depends on the domain name). These top level domain names are controlled by the Internet Assigned Numbers Authority (IANA) in a root zone datbaase which is essentially a database of all available top level domains. 
- Because all of the names in a given domnain name have to be unique there needs to be a way to organize this all so that domain names aren't duplicated. This is where domain regisrars come in. A registrar is an authority that can assign domain names directly under one or more top-level domains. There domains are registered with InterNIC, a service of ICANN, which enfores uniqueness of domain names across the internet. Each domain name becomes registered in a central database known as the WhoIS database.
- Popular domain registrars include: Amazon, GoDaddy.com, 123-reg.co.uk, etc.

3- The SOA record stores information about:
    - The name of the server that supplied the data for the zone
    - The administrator of the zoe
    - The current version of the data file
    - The default number of seconds for the time to live file on resource records.

4- NS stands for Name Server Records
    - They are used by Top Level Domain servers to direct traffict to the Content DNS server which contains the authoritative DNS records.

5- What is an A record?

- An "A" record is the fundamental type of DNS record. The "A" in A record stands for "Address". The A record is used by a computer to translate the name of the domain to an IP address.

6- What is TTL?

- The lengh that a DNS record is cached on either the Resolving Server or the users own local PC is equal to the value of the "Time To Live" (TTL) in seconds. The lower the time to live, the faster changes to DNS records take to propagate throught the internet.

7- What is a CName?

- A Canonical Name (CName) can be used to resolve one domain name to another.

8- What is an Alias Record?

- Alias records are used to map resource record sets in your hosted zone to Elastic Load balancers, CloudFront distributions, or S3 buckets that are configured as websites. A CName an;'t be used for naked domain names.

9- Routing Policies

- Simple Routing Policy
    - If you choose the simple routing policy you can only have one record with multiple ip addresees, if you specify multie values in a record, Route 53 returns all values to the user in a random order.
- Weighted Routing Policy
    - Allows you to split your traffict based on different weights assigned.
- Latency-Based Routing Policy
    - Allows you to route your traffic based on the lowest network for your end user.
    - To use latency-based routing, you create a latency resource record set for the Aamazon EC2 (or ELB) resource in each region that hosts your website. When Amazon Route 53 receives a query for your site, It selects the latency resource record set for the region that gives the user the lowerst latency Route 53 then responds with the value associated with that resource record set.
- Failover Routing Policy
    - Failover routing policies are used when you want to create an active/passove set up.
- Geolocation Routing Policy
    - Geolocation routing lets you choose where your traffict will be send based on the geographic location fo your users (ie the location from which DNS queries originate)
- Geoproximity Routing Policy
    - Geoproximity routing lets Amazon Route 53 route traffic to your resources based on the geographic location of your users and your resources. You can also optionally choose to route more traffic or less to a given resource by specifying a value, known as a bias. A bias expands or shrinks the size of the geographic region from which traffic is routed to a resource.
- Multivalue Answer Policty
    - Multivalue answe routing lets you configure Amazon Route 53 to return multiple values, such as IP addresses for your web servers, in response to DNS queries. You can specify multiple values for almost any record, but multivalue answer routing also lets you check the health of each resource, so Route 53 returns only values for healthy resources. Similar to simple routing however it allows you to put health checks on each record set.

