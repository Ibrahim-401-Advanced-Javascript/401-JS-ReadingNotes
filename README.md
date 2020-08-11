## 401 JavaScript Reading Notes

***

#### Class-01
 
##### Reading, Research, and Discussion

1. Why would you want to run JavaScript code outside of a browser?
* Running JS outside of a browser is helpful when creating CLI or back-end applications. 

2. What is the difference between a module and a package?
* A module is a single file (or set of files within one import) that are utilized by the developer.
* A package is a collection of modules. 

3. What does the node package manager do?
* NPM is used publish, discover, install, and develop node programs. [npm docs](https://docs.npmjs.com/cli/npm.html)
* It puts modules in place so that node can find them and so that dependency conflicts may be managed effectively.

4. Provide code snippets showing 3 different ways to export a function from a node module.
![module exports png](assets/module-exports.png)

##### Vocabulary

* `ecosystem`
  * the various libraries, frameworks, and programs which utilize and depend upon a common programming language 
* `Node.js`
  * an open-source development platform for developing server-side applications
* `V8 Engine`
  * a high performance engine which receives/compiles/executes code, handles the callstack, and manages memory
  * [HackerNoon](https://hackernoon.com/javascript-v8-engine-explained-3f940148d4ef)
* `module`
  * a single file, or group of files captured in one import, which contain classes or functions to be used by the developer as core features for a specific purpose
  * [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
* `package`
  * a collection of modules
* `node package manager (npm)`
  * a software registry used by developers and organizations to publish, install, and develop note programs
  * [NPM Docs](https://docs.npmjs.com/cli/npm.html)
* `server`
  * software that satisfies client requests to the web, processes network requests over HTTP, and stores/processes/delivers web pages
  * [Wiki](https://en.wikipedia.org/wiki/Web_server)
* `environment`
  * anything installed on the machine where the app is being executed: inclyuding operating system, databases, environment variables, the compilers and interpreters being used, the local network, memory space available, etc.
  * [Quora](https://www.quora.com/What-is-the-programming-environment)
* `interpreter`
  * executes instructions written in  without converting them to an object code or machine code 
  * interpreted languages include JavaScript, Perl and Python
  * [GeeksforGeeks](https://www.geeksforgeeks.org/compiler-vs-interpreter-2/)
* `compiler`
  * converts an entire program into object code, which can then be directly executed as binary code
  * compiled languages include C and C++
  * Java programs are compiled to an intermediate form, then interpreted
  * [GeeksforGeeks](https://www.geeksforgeeks.org/compiler-vs-interpreter-2/)

***

#### Class-02
 