Q1. What is an API? Give an example, where an API is used in real life.
Q2. Give advantages and disadvantages of using API.
Q3. What is a Web API? Differentiate between API and Web API.
Q4. Explain REST and SOAP Architecture. Mention shortcomings of SOAP.
Q5. Differentiate between REST and SOAP.

## Ans 1
An API, or application programming interface, enables interaction between software applications, systems, or platforms to send and receive data. An API is the messenger that delivers your data request to an external source and then returns their reply to you.

### Real life example
When searching a price comparison site, the site aggregates multiple options and showcases the cheapest ones by using third-party APIs to collect information from online travel agents or airlines.  

## Ans 2
### Benefits of using APIs
The development of APIs has enabled many business innovations and workflow efficiencies, here’s just three of the biggest benefits of using APIs:

### Automation
When using an API managed by computers, less human effort is required and workflows can be easily updated to become faster and more productive. Furthermore, new content and information can be published and shared with your entire audience quickly and efficiently across all channels. 

### Developer efficiency and innovation
APIs empower developers to be more productive by reusing code in complex but repetitive processes. They don’t need to start from scratch as the API specifies how to assemble software components in a program. APIs exist to make it easy to interface with other developers' applications.

### Improved value proposition
By using APIs made available by companies such as Amazon, Salesforce, or Twitter, an application can integrate those services into their own systems to make themselves more attractive to customers.

## API Disadvantages
There is a lot of conveniences and advantages to APIs, but business leaders should also be aware of the disadvantages. As a single point of entry, an API is a gateway and can become a hacker's primary target. Once the API is compromised, all other applications and systems become vulnerable.

Nine of the top ten vulnerabilities listed in the OWASP Top 10 now mention APIs — and since APIs can be accessed over the internet, they will have all the same disadvantages as any other Internet-based resource.  APIs are vulnerable to man-in-the-middle attacks, CSRF attacks, XSS attacks, SQL injection, and DDoS attacks.

## Ans 3 
Web API is an API as the name suggests, it can be accessed over the web using the HTTP protocol. It is a framework that helps you to create and develop HTTP based RESTFUL services. The web API can be developed by using different technologies such as java, ASP.NET, etc. Web API is used in either a web server or a web browser. Basically Web API is a web development concept. It is limited to Web Application’s client-side and also it does not include a web server or web browser details. If an application is to be used on a distributed system and to provide services on different devices like laptops, mobiles, etc then web API services are used. Web API is the enhanced form of the web application.



API is an interface that exposes an application's data to outside software, whereas web applications are one type of API with stricter requirements while Web API as the name suggests, is an API over the web which can be accessed using HTTP protocol. It is a concept and not a technology. We can build Web API using different technologies such as Java, .NET etc.



## Ans 4
SOAP is a protocol which was designed before REST and came into the picture. The main idea behind designing SOAP was to ensure that programs built on different platforms and programming languages could exchange data in an easy manner. SOAP stands for Simple Object Access Protocol.


REST was designed specifically for working with components such as media components, files, or even objects on a particular hardware device. Any web service that is defined on the principles of REST can be called a RestFul web service. A Restful service would use the normal HTTP verbs of GET, POST, PUT and DELETE for working with the required components. REST stands for Representational State Transfer.

### Shortcomings of Soap
SOAP only uses XML. It doesn’t take other formats like JSON into consideration.

There is a high possibility of coupling between client and server as SOAP is based on contract.

Since it uses XML format, SOAP is considered to be a slow platform because the payload is large for a simple string message.

Any change in server contract is reflected in client stub classes.

SOAP is hard to test in browsers.

SOAP clients do not hold any stateful references to remote objects.

## Ans 5
Key Difference Between SOAP and REST API

SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.

SOAP is a protocol whereas REST is an architectural pattern.

SOAP uses service interfaces to expose its functionality to client applications while REST uses Uniform Service locators to access to the 
components on the hardware device.

SOAP needs more bandwidth for its usage whereas REST doesn’t need much bandwidth.

Comparing SOAP vs REST API, SOAP only works with XML formats whereas REST work with plain text, XML, HTML and JSON.

SOAP cannot make use of REST whereas REST can make use of SOAP.


```python

```
