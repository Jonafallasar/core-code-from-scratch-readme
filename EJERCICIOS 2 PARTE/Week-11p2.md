# Week Challenges (Wednesday) 🐤

## APIs Core Understanding Learning Exercise 🧠

**1. What is an API?**
[source](https://www.freecodecamp.org/news/what-is-an-api-in-english-please-b880a3214a82/#:~:text=Technically%2C%20API%20stands%20for%20Application,customers%2C%20or%20for%20internal%20use.)

It stands for Aplication Programming Interface. It's an interface to a server that has some data or does some actions.

Example of the API server: When you type www.facebook.com into your browser, a request goes out to Facebook’s remote server. Once your browser receives the response, it interprets the code and displays the page. Overall, it's a block of [code](https://www.trio.dev/blog/api-examples).

**2. What is a Protocol?** Is the beginning of an URL. System of rules that allows other systems to transmit or transfer information.These are identified by the IP Address and Port Number.

![image](https://www.freecodecamp.org/news/content/images/2019/08/0-DTR8JpFZo31ht-Kd.jpg)

[source 1](https://www.freecodecamp.org/news/http-and-everything-you-need-to-know-about-it/)

[source 2](https://www.freecodecamp.org/news/what-is-an-api-in-english-please-b880a3214a82/#:~:text=Technically%2C%20API%20stands%20for%20Application,customers%2C%20or%20for%20internal%20use.)

[source 3](https://en.wikipedia.org/wiki/Communication_protocol)

**3. Is the term API only applicable to the communication of programs over the Internet?** No, it's a way for two or more computer programs to communicate with each other. Whether it has Internet or not. It is a type of software interface.

**4. Why is structured communication between two programs important?**
Because we humans cannot speak the language of the server so we need a set of instructions to help us translate the data we give to the device, so it's stored in a place where it need to be processed or analyzed, to do something with it. That way, we don't worry about our inputs and receive only the output.

[source1](https://www.freecodecamp.org/news/computer-networking-how-applications-talk-over-the-internet/)

**6. Do we humans use APIs when communicating without technology?**
I don't think so. We need a technology in order to develop machine language and make each technology to communicate with each other.

[we cannot imagine a world without APIS](https://www.influentialsoftware.com/why-apis-are-important-imagine-a-world-without-them/)

**7. Is an API just another program or a standard?** A program because the point of its usage is to communicate with another program or machine language. It implements the description of the machine language, considering standards. However, it's beyond.

**8. Do you know any API? Can you list at least 5 examples of APIs?**

1. Twitter Bots

2. Log-In Using XYZ

3. Weather Snippers

4. Pay with PayPal

5. Google Maps

[source](https://www.trio.dev/blog/api-examples)

## From JSON to REST Learning Exercise 🧠

**1. What is HTTP?**

It's the HTTP which means Hypertext Transfer Protocol this is the most basic communication between web browsers and web servers.

[source](https://developer.mozilla.org/en-US/docs/Web/HTTP)

[http&rest](https://www.freecodecamp.org/news/how-the-web-works-part-iii-http-rest-e61bc50fa0a#.vbrmrnihn)

**2. What is JSON?** It stands for JavaScript Object Notation. A lightweight format for storing and transporting data. Clearer communication between humans and machine language through parse (análisis). A standard to create information. It's a key value of sending data.

source from [freeCodeCamp](https://www.freecodecamp.org/news/what-is-json-a-json-file-example/#:~:text=What%20is%20JSON%3F,String)

**3. Is JSON the same as a plain Javascript object?**
Not at all. It's similar in Object synxtax but the way we differentiate it is by ading "" quotation marks to the attributes names.

**4. What is REST?** REST stands for REpresentational State Transfer. It is a standard that guides the design and development of processes which enable us interact with data stored on a web servers.

[source](https://www.freecodecamp.org/news/what-is-rest-rest-api-definition-for-beginners/)

**5. Is REST a programming language, framework, technology, or architecture pattern?** According to its definition, its a standard and architecture pattern.

**6. What is a Resource in REST?**

A resource is an object with a type, associated data, relationships to other resources, and a set of methods that operate on it. It is similar to an object instance in an object-oriented programming language, with the important difference that only a few standard methods are defined for the resource (corresponding to the standard HTTP GET, POST, PUT and DELETE methods), while an object instance typically has many methods. [source](https://restful-api-design.readthedocs.io/en/latest/resources.html)

[restApiTutorial](https://www.freecodecamp.org/news/rest-api-tutorial-rest-client-rest-service-and-api-calls-explained-with-code-examples/)

**7. What is a resource identifier?**

Universal Resource Identifier Patterns.The URI must contain the correct connection information to successfully call the API.

[reference](https://www.ibm.com/docs/en/streams/4.1.0?topic=reference-uri-patterns)

**8. What is an HTTP method?**
It's what allows us to request and respond the data from the application layer to the current web server or app server. It's an HTTP request method.

**9. What HTTP methods does REST use within its architecture rules?**

- Post - Create
- Get - Read
- Put/Patch - Update
- Delete - Delete

All known as CRUD operations.

**10. Why do we use HTTP methods in REST and how do they relate to resources?**
The methods allows us to start interacting with the data inputs from the client. Then, they allow us to collect them and organize them by types. This is when they turn into resources because it becomes repetitive and once we indicate them (with Query parameters) how it must be collected, as the last step it must call the API. In that way, an output from the backend can be provided.

**11. Is REST the same as HTTP?** No. The HTTP is exclusive communication between Web Browser and Web Server. From there, the REST is what happens from the Web server to the server Application (remote).

## REST API Clients Learning Exercise 🧠 

**1. Install Postman in your computer, follow [this](https://learning.postman.com/docs/getting-started/installation-and-updates/) guide**

**2. Watch [this](https://www.youtube.com/watch?v=VywxIQ2ZXw4) course about how to use Postman to interact with APIs**

**3. Answer the questions:**

- Postman only works with REST APIs? [Not necessarily](https://blog.postman.com/rest-api-examples/). Rest is only one of the many ways to project the requests and data in a visual way.
- Is there an alternative to Postman? Yes, some like [these](https://testfully.io/blog/top-5-postman-alternatives/). Postman is good just for interaction between APIs. Not between user and API. It's better to have another API and not Postman for security and performance testing.

[These](https://github.com/public-apis/public-apis) other too.

![image](https://user-images.githubusercontent.com/98929413/193908295-77913871-2e94-41ca-b98b-0c42aba69aeb.png)

## Express.JS Core Understanding Learning Exercise 🧠 

Read about the Chain of Responsibility design pattern [here](https://refactoring.guru/es/design-patterns/chain-of-responsibility).

**1. Express JS Hello World:**

- Create a new Node.JS project using NPM.
- Install Express.JS as an external dependency in your project following [this](https://expressjs.com/es/starter/installing.html) guide.

![image](https://user-images.githubusercontent.com/98929413/193936705-92a5a5f1-08fd-4a21-805c-73e4e5b5278a.png)

- Create an Express.JS Hello World application following [this](https://expressjs.com/es/starter/hello-world.html) guide.

![image](https://user-images.githubusercontent.com/98929413/193936989-3d69f02e-fb98-400b-8d63-b2551d656417.png)


![image](https://user-images.githubusercontent.com/98929413/193936847-a1078e23-7b9f-4758-9172-40c6786aed3a.png)


[source](https://www.redhat.com/es/topics/api/what-is-a-rest-api)
