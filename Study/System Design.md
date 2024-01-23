System design refers to the process of creating a high-level plan or blueprint for the architecture, component, and interactions of a complex system.
It involves designing the structure, behaviour, and functionality of the system to meet specific requirements and objectives.

### Why System Design:

System Design is essential because it enables scalability, efficiency, reliability, modularity, user experience, and effective collaboration.
It sets the foundation for successful system development and plays a crucial role in achieving the desired outcomes.
##### Examples:
- Google Material Design
- Apple Human Interface Guidelines
- Microsoft Fluent Design System
- Salesforce Lightning Design System
- Atlassian Design System
- Adobe Spectrum

## Load Balancer
##### Problem Statement:
In System Design, a common issue arises when a single server or resource becomes overwhelmed with incoming network traffic or workload, resulting in decreased performance, slow response times, and potential system failures.
This problem requires an effective solution to evenly distribute the workload across multiple servers on resources.

##### Solution
A load balancer acts as a traffic manager that evenly distributes incoming requests or workloads across multiple servers or resources in a system.
Its purpose is to optimise resource utilisation, improve performance, and ensure high availability by preventing any single component from being overwhelmed.

##### Advantages of Load Balancer
- Improved Performance
- Enhanced Scalability
- High Availability
- Efficient Resource Utilisation
- Simplified Maintenance

## Caching
##### Problem Statement
A system is getting a lot of requests, and it is taking a long time to respond.

##### Solution
The system can use a caching system to store frequently accessed data in memory. This will reduce the amount of time it takes to respond to those requests, because the system will not have to go to the database to retrieve the data.

*Caching is a technique that stores frequently accessed data in a temporary location, such as memory, to improve access speed.*

## Cache Eviction Policies
##### Problem Statement
A system has a limited amount of cache space, and it needs to decide which data to evict when the cache is full.

##### Solution
The system can use a cache eviction policy to decide which data to evict. There are many different cache eviction policies, such as least recently used (LRU), least frequently used (LFU), and random.

*A Cache Eviction Policy is a strategy for deciding which data to remove from a cache when it is full.*

## Data Partitioning
##### Problem Statement
A social media platform is experiencing high traffic and is struggling to keep up with the demand. The platform needs to find a way to improve performance without having to invest in more hardware.

##### Solution
The platform can use data partitioning to distribute the data across multiple servers. This will allow the platform to scale out and handle more traffic without having to increase the capacity of each server.

*Data Partitioning is the process of dividing a large dataset into smaller, more manageable pieces. This can be done by dividing the data based on geographical location, time, or any other criteria that makes sense for the application.*

## Data Redundancy
##### Problem
A company is storing customer data in a single database. If the database fails, the company will lose all of its customer data.

##### Solution
The company can use data redundancy to store the customer data in multiple locations. This way, if one location fails, the data will still be available in another location.

## SQL and NO SQL
##### Problem Statement
A company is building a new social media platform. The platform will need to store a large amount of data, including user profiles, posts, and comments.

##### Solution
The company can use a combination of SQL and NoSQL databases to store the data. SQL databases are well-suited for strong structured data, such as user profiles. NoSQL databases are well-suited for storing unstructured data, such as posts and comments.

## CAP Theorem
##### Problem
The CAP theorem states that in a distributed system, it is impossible to simultaneously achieve consistency (all nodes see the same data at the same time), availability (system always responds to requests), and partition tolerance (system continues to operate despite network failures).

##### Solution
When designing a distributed system, the CAP theorem suggests that you must prioritise two out of three CAP properties based on your specific requirements.

## Consistent Hashing
##### Problem Statement
A large e-commerce website needs to distribute its traffic across cluster of servers. The website wants to ensure that all requests are routed to the least loaded server.

##### Solution
The website can use consistent hashing to distribute its traffic. Consistent hashing is a technique that maps keys to servers in a way that ensures that the load is evenly distributed across all servers. When a request is received, the website can use the consistent hashing algorithm to determine which server to route the request to.

## Message Queues
##### Problem Statement
A large e-commerce website needs to process a large number of orders each day. The website wants to ensure that orders are processed in a timely manner and that they are not lost.

##### Solution
The website can use message queues to process orders. Message queues are a way of decoupling different parts of a system. In this case, the website can use message queues to decouple the order processing system from the web application.

## Content Delivery Network (CDN)
##### Problem Statement
A large e-commerce website needs to deliver its content to users all over the world. The website wants to ensure that users have a fast and reliable experience, regardless of their location.

##### Solution
The website can use a CDN to deliver its content. A CDN is a network of servers that are located all over the world. When a user requests a file from the website, the request is routed to the closest CDN server. This ensures that the user receives the file quickly and reliably.

CDNs are a popular solution for delivering large amounts of content to users all over the world. They can help to improve performance, availability, and reliability.