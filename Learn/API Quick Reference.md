## HTTP Verbs
- <b>GET:</b> Retrieve data from the server.
- <b>POST:</b> Send data to the server to create a resource.
- <b>PUT:</b> Send data to the server to update a resource.
- <b>Patch:</b> Send data to the server to update a resource partially.
- <b>DELETE:</b> Delete a resource from the server.
- <b>TRACE:</b> Returns the full HTTP request received by the server for the requested URL.
- <b>OPTIONS:</b> Returns the HTTP methods supported by the server for the requested URL.
- <b>CONNECT:</b> Converts the request connection to a transparent TCP/IP tunnel for secure communication.
- <b>PURGE:</b> Invalidates a cached resource.
- <b>LOCK:</b> Locks the resource for exclusive use by the client.
- <b>UNLOCK:</b> Unlocks the resource previously locked by the client
- <b>MKCOL:</b> Creates a new collection resource
- <b>COPY:</b> Copies the resource identified by the Request-URL to the destination URL.
## HTTP Status Codes
- 1xx : Informational
- 2xx : Success
- 3xx : Redirection
- 4xx : Client Errors
- 5xx : Server Errors

## Response Headers
- <b>Content-Type:</b> Specifies the MIME type of the data in the response body.
- <b>Content-Length:</b> Specifies the length of the response body in bytes.
- <b>Cache-Control:</b> Specifies the caching behaviour of the response
- <b>Location:</b> Specifies the URL of a resource that can be used to retrieve the requested resource.
- <b>Server:</b> Specifies the name and version of the server software that generated the response.
- <b>Access-Control-Allow-Origin:</b> Specifies which origins are allowed to access the resource.
- <b>Set-Cookie:</b> Specifies a cookie that should be stored by the client and sent back to the server with future requests.
- <b>Expires:</b> Specifies the date and time after which the response is considered stale.
- <b>Last-Modified:</b> Specified the date and time the resource was last modified.

## API Design
- <b>REST:</b> Representational State Transfer, a design pattern for building web services
- <b>SOAP:</b> Simple Object Access Protocol, a messaging protocol for exchanging structured data
- <b>GraphQL:</b> A query language and runtime for building APIs
- <b>API Gateway:</b> A service that manages, protects, and scales APIs

## API Architectures
- <b>SOA:</b> Service-Oriented Architecture, an architectural style for building distributed systems
- <b>Microservice:</b> An architectural style for building complex applications as a suite of small, independent services
- <b>Serverless:</b> A cloud computing execution model where the cloud provider manages the infrastructure and automatically allocates resources as needed
- <b>Event-Driven:</b> An architectural style where the flow of data between components is triggered by events
- <b>RESTful API:</b> An architectural style that uses HTTP requests to GET, POST, PUT, and DELETE data.

## API Design Patterns
- <b>Adapter Pattern:</b> A pattern that converts the interface of a class into another interface that clients expect.
- <b>Decorator Pattern:</b> A pattern that adds behaviour to an individual object dynamically
- <b>Proxy Pattern:</b> A pattern that provides a surrogate or placeholder for another object to control access to it.
- <b>Chain of Responsibility Pattern:</b> A pattern that delegates commands to a chain of processing objects
- <b>Observer Pattern:</b> A pattern that defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

## API Security
- <b>OAuth:</b> An open standard for authorisation used for protecting APIs.
- <b>JWT:</b> JSON Web Tokens, a standard for securely transmitting information between parties as a JSON object.
- <b>SSL/TLS:</b> Secure Sockets Layer/Transport Layer Security, a protocol for establishing a secure connection between a client and a server.
- <b>API Key:</b> A secret token used to authenticate API requests.
- <b>Rate Limiting:</b> A technique used to limit the number of requests that can be made to an API over a specific period of time.
- <b>OpenID Connect:</b> An authentication layer built on top of OAuth that allows users to be authenticated across multiple domains.
- <b>Cross-Origin Resource Sharing (CORS):</b> A mechanism that allows many resource (e.g., fonts, JavaScript, etc.) on a web page to be requested from another domain outside the domain from which the resource originated.

## API Testing
- <b>Postman:</b> A popular tool for testing and debugging APIs
- <b>SoapUI:</b> A tool for testing SOAP and REST web services
- <b>Swagger:</b> A tool for designing, building, and testing APIs
- <b>JMeter:</b> A tool for testing the performance of APIs
- <b>TestRail:</b> A test management tool for planning, executing, and tracking API tests
- <b>Dredd:</b> A command-line tool for testing API documentation against its backend implementation
- <b>REST Assured:</b> A Java-based library for testing RESTful APIs
- <b>Karate DSL:</b> A testing framework for API Testing using Gherkin syntax
- <b>HttpMaster:</b> A tool for testing and debugging APIs
- <b>Assertible:</b> A tool for testing and monitoring APIs with automated tests.

## API Development
- **Node.js:** A JavaScript runtime for building server-side applications.
- **Express:** A popular framework for building web applications and APIs with Node.js
- **Django:** A Python web framework for building web applications and APIs.
- **Flask:** A lightweight Python web framework for building web applications and APIs.
- **Spring:** A Java framework for building enterprise-level web applications and APIs.
- **Swagger Editor:** A tool for designing and documenting APIs using the OpenAI specification.
- **Postman:** A tool for designing and debugging APIs.
- **Insomnia:** A tool for designing, testing, and debugging APIs.
- **Paw:** A tool for designing and testing APIs on Mac OS.
- **API Blueprint:** A high-level  API description language for building RESTful APIs.

## API Implementation Platforms
- **Firebase:** A mobile and web application development platform developed by Google.
- **Backendless:** A mobile and web application development platform that allows developers to build and deploy applications without backend coding.
- **Parse Server:** An open-source version of the Parse backend that can be deployed to any infrastructure.
- **Amazon API Gateway:** A fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs.
- **Microsoft Azure API Management:** A fully managed service that enables users to publish, secure, transform, maintain, and monitor APIs.

## API Performance
- **Caching:** A technique for improving API performance by storing responses in a cache.
- **Throtting:** A technique for limiting the rate of requests to an API to prevent overload.
- **Load Balancing:** A technique for distributing traffic evenly across multiple servers to improve API Performance.
- **Content Delivery Network (CDN):** A distributed system of servers that delivers content to users based on their geographic location to improve API Performance.
- **Edge Computing:** A computing paradigm that brings computation and data storage closer to the location where it is needed to reduce latency and improve API Performance.

## API Monitoring
- **Pingdom:** A tool for monitoring the uptime and performance of APIs.
- **New Relic:** A tool for monitoring the performance of APIs and other web applications.
- **Datadog:** A monitoring and analytics platform for cloud-scale applications and APIs.
- **Sumo Logic:** A cloud-based log management and analytics platform for API and other applications.
- **Loggly:** A cloud-based log management platform for monitoring APIs and other applications.

## API Standards
- **JSON API:** A specification for building APIs that use JSON as the data format.
- **HAL:** Hypertext Application Language, a standard for building hypermedia-driven APIs.
- **JSON-LD:** A format for representing linked data on the web.
- **OData:** Open Data Protocol, a standard for building and consuming RESTful APIs.
- **AsyncAPI:** A specification for building event-driven APIs.

## API Standard Organisations
- **W3C -** The World Wide Web Consortium, an international community that develops web standards.
- **IETF -** The Internet Engineering Task Force, an open standards organisation that develops and promotes Internet standards.
- **OASIS -** Organisation for the Advancement of Structured Information Standards, a non profit consortium that drives the development, convergence, and adoption of open standards for the global information society.
- **RESTful API Modeling Language (RAML) -** A YAML-based Language for describing RESTful APIs developed by MuleSoft.
- **JSON API -** A specification for building APIs that use JSON as the data format.

## API Infrastructure
- **Kubernetes:** An open-source platform for managing containerised workloads and services
- **OpenShift:** A container application platform that builds on top of Kubernetes.
- **Docker Swarm:** A native clustering and orchestration solution for Docker.
- **Consul:** A service mesh solution that provides service discovery, configuration, and segmentation capabilities.
- **Istio:** A service mesh solution that provides traffic management, security, and observability capabilities.

## API Governance
- **API Management:** The process of creating, publishing, and monitoring APIs in a secure and scalable way.
- **API Monetisation:** The process of generating revenue from APIs by charging developers for usage.
- **API Versioning:** The process of managing changes to APIs over time.
- **API Analytics:** The process of collecting and analysing data on API usage and performance.
- **API Gateway:** A service that manages, protects, and scale APIs.

## API Documentation
- **OpenAPI:** A specification for building APIs in YAML or JSON format.
- **API Blueprint:** A high-level API description language for building RESTful APIs.
- **RAML:** A YAML-based language for describing RESTful APIs.
- **Swagger UI:** A tool for visualising and interacting with APIs that have been described using OpenAPI specification.
- **State:** A tool for generating beautiful, responsive API.

## API Deployment
- **Heroku:** A cloud platform for deploying, managing, and scaling web applications and APIs.
- **AWS Elastic Beanstalk:** A service for deploying and scaling web application and APIs on AWS.
- **Azure App Services:** A service for deploying and scaling web applications and APIs on Azure.
- **Google App Engine:** A service for deploying and scaling web applications and APIs on GCP.
- **Docker:** A containerisation platform used for packaging and deploying applications.
- **AWS Lambda:** A serverless compute service for running code in response to events.
- **Azure Functions:** A serverless compute service for running code in response to events.
- **Google Cloud Functions:** A serverless compute service for running code in response to events.
- **Netlify:** A cloud platform for deploying and managing static websites and APIs.
- **Vercel:** A cloud platform for deploying and managing static websites and APIs.

## API Best Practices
- **Versioning:** A technique for managing changes to APIs over time.
- **Pagination:** A technique for breaking up large API responses into smaller, more manageable chunks.
- **Caching:** A technique for improving API performance by storing responses in a cache.
- **Error Handling:** A technique for returning meaningful error messages to API clients.
- **HATEOAS:** Hypermedia as the Engine of Application State, a constraint of RESTful APIs that requires the API to provide links to related resources.

## API Tools
- **API Studio:** A web-based IDE for designing and testing APIs.
- **Stoplight:** A collaborative platform for designing, documenting, and testing APIs.
- **Apigee:** A full lifecycle API management platform that allows developers to design, secure, deploy, and analyse APIs.
- **Azure API Management:** A fully managed service that enables users to publish, secure, transform, maintain, and monitor APIs.
- **Postman Learning Center:** A hub for learning how to use Postman to design, develop, and test APIs.