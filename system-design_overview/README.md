# SYSTEM DESIGN
The system design is the most important part of the project. It is the part that will determine the success of the project. 

Its a step by step  process of defining a particular software architecture,module, components and etc.

*Interviewers like Google,Microsoft and Amazon ask questions on it to check the interviewers ability to think about building apps architecture from scratch.

## Need for System Design
system design is used to prepare the architecture of the software or application.
A developer asks for the requirements of the app which are functional and non functional.

* Non-functional requirements include scalability, high availability, consistency, etc.

Afterwards a developer comes up with a picture and prepares the architecture for application according to requirements.e.g consider whether to use sql or Nosql database on data.

* Companies like google  and FB have multiple servers worldwide and serve the resources to users from the nearest server to make their applications efficient. This is also a part of the system design.

## Exploring Essential Design Methods in System Design
There are many design methods that are used in system design. Some of them are:
 

 ### 1. Architectural Design
 Architectural design is the process of defining a system's overall structure, including its components, their relationships, and the principles that guide their interaction.


it includes client-server interaction.

### 2. ERD Diagram
ERD diagram is a visual representation of the entities and their relationships in a database. It is used to model the structure of a database and to communicate

### 3. UML Diagram
Unified Modelling Language diagram is a visual representation of the structure and behavior of a software system. 

It contains different diagrams like activity diagrams, class diagrams, sequence diagrams, etc., to represent the different aspects of the system.

### 4. Class Diagrams
They are used to represent classes.They can also contain attributes,methods and relationships between multiple classes.

### 5. Sequence Diagrams
The sequence diagrams represent the interaction between the various components of the system. It is used to model the behavior of the system.

## Diving Deeper into System Design Concepts
### 1. Performance vs Scalability
Performance and scalability are two important aspects of system design.
* Performance refers to the speed and efficiency of the system.
* Scalability refers to the ability to scale the application.

ie. Some websites takes more time to load than others. Those that load slower scare away visitors. this is due to low performance

Scalability is seen where a an app becomes more popular and hence recieving more requests.,eg google.

Google therefore has  have worldwide data centers for distributing the load. When the number of users increases, they either increase the capacity of a particular server or develop a new server.

### 2. Latency vs Throughput
<b>Latency </b>The latency is a measurement of the time delay to complete a single request or data operation.

Its mainly crusial in live gaming and online videocalls.

Its a network delay that occurs to geographical distance,transport protocol and its measured in milliseconds.

<b>Throughput</b>is the number of operations the system can handle in a particular time.

Measured in mbs and its used to check the capability of a system.

### 3. Consistency Patterns and Availability Patterns
<b>Consistency:</b> Consistency ensures that all nodes in the system read the same data at a particular time.
eg Bank accounts.

<b>Availability</b> The system's availability ensures that each request receives a response either with fresh or old data. The availability is important when high uptime is needed.

<b>Consistency Patterns</b>
* Strong consistency: Strong consistency ensures that each request should get the most recent data. To achieve strong consistency, you require synchronized communication. It prioritizes consistency over availability.
* Eventual Consistency: Eventual consistency allows temporary inconsistencies to be resolved soon. It prioritizes availability over consistency.
* Weak Consistency: In the weak consistency pattern, the user may get fresh data after writing the data. It focuses on the fast access. It can be used in live streaming or video chat.

<b>Availability Patterns</b>
* Load Balancing: The upcoming request can be distributed across multiple servers to achieve high availability
* Retry and timeout strategies: You can implement the retry mechanism to process the request after every interval if the system fails or is not available.eg,refreshing your website.

## Advanced Concepts in System Design
### 1. CDN
Content delivery network is a distributed server network located at different geo-locations. The CDN is used to deliver content like images, various data, etc., from the server.

It delivers the resource faster, decreases latency and improves the application's performance.

** When users request a particular resource, the application requests the nearest server. If the nearest server has cached resources already, it serves it directly. Otherwise, it requests the origin server, caches the resources, and delivers them to the users. Next time, when the server gets a request for the same resource, it will return the cached resources.

### 2. DNS
The DNS system allows users to access the website and its resources using the domain name (e.g., www.example.com). 

** It maps the unique domain name with a unique IP address. So, whenever you make a request for the resources of the particular domain name, it returns the resources of IP addresses, which are mapped with the domain name


### 3. Caching
Caching is a mechanism to serve resources faster. Its a high-speed storage that works between the web application and the source of the data.

e.g, when you make a request for some data, the application checks first in the cache storage. If data exists in the cache storage, it returns the data. Otherwise, it requests the database

### 4. Proxies
The proxy server works between the client of the application and the internet. 

Whenever you request to get resources from the internet, the application requests the proxy server, and the proxy server gets resources and sends them back to the application.

## Components of System Design
### 1. Microservices and Service Discovery
The microservices break down complex applications into small services, such that each service works independently and accomplishes specific tasks.

Concepts related include 

<b>Service Identification:</b> Every microservice has a unique ID and name for its identification.

<b>Dynamic Service Discovery:</b> Each microservice can dynamically find other services located in the same network. So, scaling and load balancing become easy.

### 2. Database Systems: RDBMS and NoSQL
<b>RDBMS</b> Relational database management system
es SQL database stores structured data.

It makes it easier to access the data from the database and connect it with other data as they are stored in the table format.

#### characteristics of the RDBMS database.

* It stores the data in the table format.
* You can’t scale the RDBMS database horizontally, but you can scale it vertically.
* SQL is a query language for the RDBMS databases.
* Accessing data from the RDBMS database is slow.

<b>NoSQL</b>

 It stores the data in the key-value pair instead of in table format.

 it used when you want  you are required to store unstructured data in the database.

 #### Characteristics of the NoSQL database.

* It stores the data in the key-value pair format.
* NoSQL database is horizontally scalable, as you can add new key-value pairs for new attributes.
* Each record can contain different key-value pairs.
* It is faster than RDBMS databases.
* It supports frequent changes in the database.

### 3. Communication Protocols
Protocols mean rules and communication protocols refer to the rules to communicate or exchange the data between two systems.

* <b>HTTP/HTTPS </b>  
HTTP is a hypertext transfer protocol.   
 HTTPS is a secure version of HTTP.    
 They are used in web-based communication.   
 It is a good idea to use HTTPS always for security reasons.
 * <b>TCP/IP:</b>  
 Transmission control protocol is used to communicate over the internet. For example, it is used in the chatting application.
* <b>UDP :</b>
User datagram protocol is mainly used for live streaming, video calls, etc., in which data loss can be tolerable.
* <b>WebSockets:</b>
 The web sockets are used for bi-directional duplex communication. It builds the connection between two web application.

 ## Approaching System Design Interview Questions
 ### Step-by-step Guide
 #### 1. Requirements clarification
 Know the requirements. Both functional and non functional.   
 <b>Function requirements:</b> are the requirements in the application with which the user interacts. For example, authentication, navigation,  etc.

<b>Non-function requirements:</b>are the requirements to improve the application's capabilities.eg, high availability, scalability, consistency, low latency, high throughput, etc.

You should move on to the next step according to the application's requirements.
#### 2. Estimation of resources
It involves deciding what kind of resources you should use to build the application.
eg. while selecting the resources for the server, you should keep in mind how howmany requests it will receive per day or second and also the data you require to store in the database.

#### 3.System interface definition
The third step is designing the system interface.
For example, defining the API endpoints and what to expect from each API endpoint.

#### 4. Defining Data model
This involves selecting the database you want to use.   
For example, if you want to store the data in the relational database, you should define the table structure and the relationship between the tables.

If you are building social media applications like Facebook or Twitter, you can easily use Graph databases to manage many-to-many relationships.


#### 5. High-level design
This step involves designing the high-level architecture of the application.   
It should be step by step.
Here you need to decide how you will connect the components of the system with each other. For example, connecting the server with the database and integrating the third-party tools with the applications.

You fulfill the functional requirements of the application.

#### 6. Detailed design
Its done after designing the application of which you improve the system design

You need to analyse the design to fufil the non functional requirements.

<b>You can analyze it as given below.</b>

* How to use caching to improve the performance of the application?
* How do we scale the application via load balancing?
* Should you use the CDN for caching, or are cookies enough?
* How would you handle the failure of the application?
* Should you distribute the data across multiple databases?
* How will you replicate the database?

#### 7. Identifying and resolving bottlenecks
lastly you should identify the bottlenecks in your system design and discuss the solutions to resolve them with the interviewer.

Examples include 
* Can the system fail in any scenario? If yes, how will you handle it?
* How do you monitor the performance of the system and issues in the system?
* Do you have enough replicas of the database to handle the failure
* How do you handle the failure of the database?
* How do you handle the failure of the server?

## Sample System Design Interview Questions and Solutions
### 1. How would you design a URL Shortening service similar to TinyURL?
#### Solution
1. I would use the REST API to communicate with the server. The API endpoint for shortening a URL can accept a POST request with the long URL as the input and return the shortened URL in the response. Another API endpoint can be used to redirect the short URL to the original long URL when clicked.
 
2.To handle 500 requests per second, I can implement load balancing techniques such as using a load balancer to distribute incoming traffic across multiple servers. This will help in scaling the service as needed to handle a high volume of requests.

3.I would use a relational database to store the mapping between the long URLs and their corresponding shortened URLs. This will allow  efficiently retrieval of the original URL when a shortened URL is accessed. Since the focus is on handling 500 requests per second and not requiring horizontal scaling, a relational database should be sufficient for this purpose.

4. The table in the relational database can have columns to store the long URL, the shortened URL, the creation timestamp, the expiry timestamp (if URL expiration is implemented), and the number of clicks on the URL. This table structure will help in efficiently managing and tracking the URLs.

5. To shorten the long URL, we can generate a unique identifier (such as a random alphanumeric string) for each shortened URL and store it in the database along with the original long URL. When a user requests a shortened URL for a long URL, we can check if the long URL already exists in the database and return the corresponding shortened URL. If not, we can generate a unique identifier, create a mapping in the database, and return the shortened URL.

### 2. How would you design a Web Crawler?
The Web crawlers allow to extract the information from different web pages.
#### Solution
1. I would start by defining what you want to extract and from where and  use a multi-threaded approach to crawl the web pages. Each thread can be assigned a specific domain to crawl, and the threads can communicate with each other to avoid duplicate crawling of pages. This will help in parallelizing the crawling process and improving the efficiency of the crawler.

### 3. How would you design Facebook and Instagram?
#### Solution
1. I would start by defining the requirements of the application, such as the features it should have
2. I would then design the database schema to store the data required by the application. This includes users relationships, posts and media metadata.

3.  Chat feature: Use WebSockets for real-time messaging or integrate third-party chat apps.
4. I would then design the API endpoints to communicate with the server. This includes
* User authentication and authorization:Implement secure methods like OAuth or JWT tokens.
* User profile management
* Post creation and deletion
* Media upload and deletion
* Comment creation and deletion
* Like and unlike functionality

5. Use Algorithms: Sort posts based on timestamp for latest posts, and use engagement metrics for trending posts.
6. Scalability: Utilize database replication for high availability, and implement data caching and load balancing for optimal performance.

### 4. How would you design the API rate limit?


















