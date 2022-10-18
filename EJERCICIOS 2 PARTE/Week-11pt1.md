# Week Challenges (Monday) 💻

Time to catch up ⏱️ or play with the React project

# Week Challenges (Tuesday) 🐣

## Node.JS Core Understanding Learning Exercise 🧠

**1. What is Node.JS?** Node is a runtime environment (entorno de ejecución) that allows JavaScript to track where functions are called considering that the stack only excecutes one function at a time. Version to use JavaScript in a server. Its creator is Ryan Dahl. It's based on V8 from Chrome.

**2. What problem does Node.JS solve?**
[Looking for personal opinions](https://www.quora.com/What-is-Node-js-really-trying-to-solve-Is-there-a-technology-mature-enough-to-choose-as-an-alternative-for-Node-js), we encounter Node.JS mainly solves allowing to use a collection of JS libraries. Allows to use ECMAScript. There are no vendor controlling the server-side options. Also, allows order and organization un functions running.

**3. What is the V8 Javascript Engine?**
It's another engine that runs JavaScript code. Used mostly in browsers. V8 can run the JavaScrip code both outside and inside a browser. This makes possible the scripting coming from the server. It helps translate the machine language. Runs to compile code. [source](https://www.cloudflare.com/es-es/learning/serverless/glossary/what-is-chrome-v8/)

**4. Is Node.JS really necessary in the Development ecosystem?**
Yes, because before using Stack or executing in the Browser architecture, it was too complicated to run the language. Now, the place where all the functions are run, is moved to a Stack beyond the browser. This allows to run only the operational architecture of the computer language without Browser dynamics interfering. This would also reduce the cost of making it.

Source: [33 concepts every developer must know](https://github.com/leonardomso/33-js-concepts)

**5. What is the difference between Node.JS and any other browser?**
NodeJs can directly run from the file system and have unrestricted access to the network unlike browsers, where these just provide sandbox (isolated testing). Building apps that run in the browser is a completely different thing than building a Node.js application.
[source](https://nodejs.dev/en/learn/differences-between-nodejs-and-the-browser/)

**6. What is NVM and Why is it useful for Node.JS developers?**
NVM stands for Node Version Managery and it's very useful for NodeJs developers because it allows developers to install different versions of node via the command line. Also, it's the largest ecosystem of open source libraries in the world and it's lightweight.

According to [Microsoft](https://learn.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-windows), Node has its own Package Manager and alternative versions.

It manages the dependencies of the project. It will install the packaged the project needs.

**7. What is sandboxing?** A sandbox is an isolated testing environment that enables users to run programs or open files without affecting the application, system or platform on which they run.

## Node.JS Module System Core Understanding Learning Exercise 🧠

**1. What is a Javascript Module?** A node Module is a reusable block of code. A system of modules are blocks of code that allows communication different parts of the code.
[source](https://www.freecodecamp.org/news/what-exactly-is-node-js-ae36e97449f5/)

**2. Why are Javascript Modules necessary?** Provides functionality to interact with the file system. It contains sample codes based on client-server classes.You create modules to better organize and structure your codebase. You can use them to break down large programs into smaller, more manageable, and more independent chunks of code which carry out a single or a couple of related tasks
[source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)

**3. What module standards are available in Node.JS?** [CommonJs](https://nodejs.org/api/modules.html) y [ECMAScript](https://nodejs.org/api/esm.html).

**4. What are the differences between ESModules and CommonJS modules?** CommonJs is the default used in Node Js while ESModules are the ECMAScript Modules, the official system of JavaScript to modules management. Para CommonJs se usa el "require()" y en ECMAScript es import {objeto} from "./folder";

**5. Which types of modules exist in Node.JS?**
[these](https://nodejs.org/api/modules.html) Mainly, Core Modules (they are already installed when you download Node Js), Local Modules(the files we create for our project) and Third Party Modules (the NPM).

**6. What's a JS runtime?** A JavaScript runtime is a set of tools that allows us to execute javascript code.

## Node.JS Module System Practice 💻 

Time to put into practice what you learned about Node.JS modules 😁.

Create a new Node.JS project, name it: your-nickname/modules

Used:
```
  npm init -y
```
  
![image](https://user-images.githubusercontent.com/98929413/193666963-80016ee4-02b1-4a54-a60d-1f840cd07bc7.png)


Create a new module, name it: operations.js

Inside operations.js implement two functions, one for the sum operation and one for the subtract operation.

![image](https://user-images.githubusercontent.com/98929413/193688367-bb8d1c1c-9fbc-436a-aa26-a186122960ed.png)

Import the functions implemented in operations.js and use them in any way in main.js.

![image](https://user-images.githubusercontent.com/98929413/193690145-94094c8c-a96b-4623-ac2c-674ecb36a571.png)

We can observe how my code editor insists on repairing the import syntax for CommonJs.

![image](https://user-images.githubusercontent.com/98929413/193691057-e8c327ea-7880-4802-a9cc-950d7e7c9176.png)

We can also observe how in this other export, it insists to convert to module "ES" for modern practices.

![image](https://user-images.githubusercontent.com/98929413/193676556-9187652a-e3e2-478d-8537-a56c7e19b699.png)

This is the final installation package characteristics.

![image](https://user-images.githubusercontent.com/98929413/193676981-23738d99-4302-4cec-988b-28cb17faddb8.png)

Finally, here's the run of the functions:

![image](https://user-images.githubusercontent.com/98929413/193690461-b120682b-c20d-4134-9881-1dbc4409605c.png)


## Client-Server Model Learning Exercise 🧠

**1. What is a Server?** The Backend. Where the data from the client is stored. Where the public website lives.

Hardware server: the physical computer that serves up web pages.

Software server: The program that runs to serve up the web pages(Apache).

**2. What is a Client?** The Frontend.Where the User inputs data and where the data from the server returns. Our devices or a device that runs some kind of web browser.

**3. Is a server just another physical computer?** Not necessarily, is just another machine language. Be a Web server or what will handle the data input by the user. It can be interpretet as a Stack both visually and verbally.

**4. Why do we refer to a certain class of applications as Servers?**
Because that's where the requests of the users are stored. There has to be a translator like a server-side programming language that will allow send the information back and forth.

**5. What is the difference?**

1.Web Server:It's the HTTP which means Hypertext Transfer Protocol this is the most basic communication between web browsers and web servers.

1.1.Web Browser Software: Software that runs on the client that displays web pages.

2.Application Servers: A software placed on server-side. Helps deliver Backendlogic of any application. Processes power and memory unit for running time. Here lays the protection of data and end-user traffic and network.[source](https://www.ibm.com/docs/en/was/9.0.5?topic=administering-introduction-application-servers)

3.Database: collection of data.

![image](https://digitalthinkerhelp.com/ezoimgfmt/i.ibb.co/TR0zkrs/applicatio-server.png?ezimgfmt=rs:712x357/rscb1/ngcb1/notWebP)

**6. Is there any similarity between human communication and the client-server model?** Yes, for example when we go to a restaurant or when we are asking for Tech support in customer service. We still exchange requests back and forth.

**7. Is the client-server model applicable only to the Web?** Yes.

**8. Can you mention any other example of this model outside the Web?** [Peer-to-peer](https://es.wikipedia.org/wiki/Peer-to-peer) and [blockchain](https://www.youtube.com/watch?v=yubzJw0uiE4). Where there are no web servers only networks.

[about server-client](https://www.freecodecamp.org/news/how-the-web-works-part-ii-client-server-model-the-structure-of-a-web-application-735b4b6d76e3/)

**Some other terminology:**

We match the domain name with the IP Address to identify them better.

Internet Service Providor: AT&T, TELMEX, etc.

The router connects the IP Address to the individual devices.

The cloud: Another name for the Internet.

HTTP/HTTPS: Hypertext Transfer Protocol - foundation of data communication for the web. With the "S" at the end it means "secure", aids in security during data transmission (incrypts).
