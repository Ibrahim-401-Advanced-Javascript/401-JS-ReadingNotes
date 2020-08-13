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
    * NPM is used publish, discover, install, and develop node programs. 
      * [npm docs](https://docs.npmjs.com/cli/npm.html)
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
    * [hackernoon](https://hackernoon.com/javascript-v8-engine-explained-3f940148d4ef)
* `module`
  * a single file, or group of files captured in one import, which contain classes or functions to be used by the developer as core features for a specific purpose
    * [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
* `package`
  * a collection of modules
* `node package manager (npm)`
  * a software registry used by developers and organizations to publish, install, and develop note programs
    * [npm docs](https://docs.npmjs.com/cli/npm.html)
* `server`
  * software that satisfies client requests to the web, processes network requests over HTTP, and stores/processes/delivers web pages
    * [wiki](https://en.wikipedia.org/wiki/Web_server)
* `environment`
  * anything installed on the machine where the app is being executed: inclyuding operating system, databases, environment variables, the compilers and interpreters being used, the local network, memory space available, etc.
    * [quora](https://www.quora.com/What-is-the-programming-environment)
* `interpreter`
  * executes instructions written in  without converting them to an object code or machine code 
  * interpreted languages include JavaScript, Perl and Python
    * [geeksforgeeks](https://www.geeksforgeeks.org/compiler-vs-interpreter-2/)
* `compiler`
  * converts an entire program into object code, which can then be directly executed as binary code
  * compiled languages include C and C++
  * Java programs are compiled to an intermediate form, then interpreted
    * [geeksforgeeks](https://www.geeksforgeeks.org/compiler-vs-interpreter-2/)

***

#### Class-02

##### Reading, Research, and Discussion

1. Name 3 advantages to Test Driven Development.
    * Writing code test-first requires you to develop more specific code with clearer aims
    * Reduction of time spent on reworking/refactoring
    * Ability to quickly identify errors and problems

2. In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?
    * If the output of another test is interfering with the outcome of another, we can 'set up' the test environment with `beforeEach()` or 'tear down' the environment with `afterEach()`
      * [jestjs.io](https://jestjs.io/docs/en/setup-teardown)
 
3. What is one downside of  Test Driven Development?
    * Development feels slower in the beginning, since making tests upfront takes a lot of time and effort. 

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
    * Constructors create Objects, and Prototypes amend/add to those Objects
    * Classes use constructors and methods to create Objects
      * [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

5. Name a use case for a static method.
    * When we need to implement functions that belong to the class, but not necessarily any particular object (instance) of it
    * For example, if we need a function to compare objects of a class, we need to create a static method within the class that targets the objects of that class
      * [js.info](https://javascript.info/static-properties-methods)

6. Write an example of a Higher Order function and describe the use case it solves.
![callback](assets/callback.png)
    * In the above example, `isEven()` is a higher-order function
    * Higher-order functions operate on other functions, either by taking them as arguments or by returning them (i.e. any function that takes a callback)
    * Higher-order functions allow us to create smaller, more readable functions to execute smaller pieces of logic (and then use those smaller functions in the higher-order functions)
      * [eloquent js](https://eloquentjavascript.net/05_higher_order.html)

##### Vocabulary

* `functional programming`
  * the process of building software using pure functions, avoiding shared state, mutable data,and side-effects
    * [medium](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)
* `pure function`
  * a function which, given the same input, will always return the same output and produces no side effects
    * [medium](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976)
* `higher-order function`
  * any function which operates on other functions, either by taking them as arguments or by returning them
    * [eloquent js](https://eloquentjavascript.net/05_higher_order.html)
* `immutable state`
  * values of the properties attached to an object will not change over time
    * [stackexchange](https://softwareengineering.stackexchange.com/questions/235558/what-is-state-mutable-state-and-immutable-state)
* `object`
  * a container for properties/values and methods/actions
* `object-oriented programming (OOP)`
  * an approach to software development in which the data structure becomes an object which includes both properties and functions(methods)
  * allows us to create relationships between objects and for objects to inherit from one another
    * [webopedia](https://www.webopedia.com/TERM/O/object_oriented_programming_OOP.html#:~:text=Object%2Doriented%20programming%20(OOP),applied%20to%20the%20data%20structure.)
* `class`
  * functions which use constructors and methods to create objects
    * [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
* `prototype`
  * a javascript property which allows us to add new properties or methods to object constructors
    * [w3schools](https://www.w3schools.com/js/js_object_prototypes.asp)
* `super`
  * the keyword used to access and call functions on an object's parent class
    * [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)
* `inheritance`
  * private properties linking javascript objects from the highest parent object to its last child object
    * [mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
* `constructor`
  * a method for creating and initializing an object of a given class
* `instance`
  * one object of a given class OR
  * one `new Object()` created from a constructor
* `context`
  * the value of `this` 
  * (think: 'in which object am i operating?')
* `this`
  * the object that owns the code being executed currently
* `Test Driven Development (TDD)`
  * a style of programming characterized by writing a single unit test first, then writing just enough code to make the test pass, then refactoring for simplicity, then repeating, accumulating unit tests over time
    * [agile alliance](https://www.agilealliance.org/glossary/tdd)
* `Jest`
  * a javascript testing framework
    * [jestjs.io](jestjs.io)
* `Continuous Integration (CI)`
  * the process of merging all devs' working copies to a shared main branch repeatedly throughout the development process
* `unit test`
  * tests to check single parts of code to ensure that they run as expected & return an expected output
    * [freecodecamp](https://www.freecodecamp.org/news/how-to-start-unit-testing-javascript/)

***

#### Class-03

##### Reading, Research, and Discussion

1. Why would a developer choose to make data models?
    * A well-done data model can make complex applications more scalable; gaining direct access to app infrastructure can make navigating changes more simple
      * [hackernoon](https://hackernoon.com/making-a-case-for-domain-modeling-17cf47030732)
2. What purpose do CRUD operations serve?
    * Allowing for persistent storage within applications/databases
      * [stackify](https://stackify.com/what-are-crud-operations/)
3. What kind of database is Postgres? MongoDB?
    * Postgres is a relational database
    * MongoDB is a non-relational database
4. What is Mongoose and why do we need it?
    * Mongoose is an object modeling tool designed for use with MongoDB.
      * [freecodecamp](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)
5. Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.
    * Table - a collection of related records within a database
    * Record - a single line with a unique ID within a database table 
      * `(Object{id})`
    * Field - a single piece of data within a record 
      * `({property: value})` 

##### Vocabulary

* `database`
  * an organized collection of information, accessed electronically via query languages
* `data model`
  * a diagram of organized elements of data which illustrates how those elements of data relate to one another
    * [hackernoon](https://hackernoon.com/making-a-case-for-domain-modeling-17cf47030732)
* `CRUD`
  * Functions of Persistent Storage: Create, Read, Update, Delete
    * [stackify](https://stackify.com/what-are-crud-operations/)
* `schema`
  * a skeleton structure representative of the logical view of an entire database
    * [tutorials point](https://www.tutorialspoint.com/dbms/dbms_data_schemas.htm)
* `sanitize`
  * the process of removing data with the purpose of making it unrecoverable
  * generally used to protect systens from malicious data
    * [medium](https://medium.com/@abderrahman.hamila/what-sanitize-mean-and-why-sanitize-in-code-data-5c68c9f76164)
* `Structured Query Language (SQL)`
  * the standard language for relational database management
    * [sqlcourse](http://www.sqlcourse.com/intro.html)
* `Non SQL (NoSQL)`
  * non-relational databases which provide flexible schemas, scale easily, and can handle large amounts of data and high user loads
    * [mongodb](https://www.mongodb.com/nosql-explained)
* `MongoDB`
  * a NoQL document-oriented database program
    * [mongodb](https://www.mongodb.com/)
* `Mongoose`
  * an object modeling tool designed for use with MongoDB
    * [freecodecamp](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)
* `record`
  * a basic data structure composed of collections of elements
    * [wiki](https://en.wikipedia.org/wiki/Record_(computer_science))
* `document`
  * JSON data stored in a database 
    * [mongodb](https://www.mongodb.com/document-databases)
* `Object Relation Mapping (ORM)`
  * a programming technique for bridging between objects and tables
  * ORM libraries take care of the bridging mechanics and
  * allow the user to interact directly with the objects in the user's preferred language
    * [stackoverflow](https://stackoverflow.com/questions/1279613/what-is-an-orm-how-does-it-work-and-how-should-i-use-one)

***

#### Class-04

##### Reading, Research, and Discussion

1. Give one strong argument for and against NoSQL Databases.
    * Pro: Flexible Data Models
      * NoSQL Databases easily store and combine any type of data, whether structured or unstructured. Schemas can be updated dynamically when needed without downtime or interruption
        * [mongodb](https://www.mongodb.com/scale/nosql-databases-pros-and-cons)
    * Con: Sacrificing referential integrity/data consistency for speed
      * With SQL Databases, we are bound by referential tables
      * With NoSQL Databases, we aren't imposing any logical consistency across tables by default; instead we need to build integrity mechanisms into the code
        * [quora](https://www.quora.com/What-are-the-pros-and-cons-of-NoSQL-databases)
2. Name 3 cloud based NoSQL Databases
    * Amazon DynamoDB 
      * [aws](https://aws.amazon.com/dynamodb/)
    * Oracle 
      * [oracle](www.oracle.com)
    * MongoDB Atlas 
      * [mongodb](https://www.mongodb.com/cloud/atlas)

##### Vocabulary
* `database`
  * an organized collection of information, accessed electronically via query languages
* `data model`
  * a diagram of organized elements of data which illustrates how those elements of data relate to one another
    * [hackernoon](https://hackernoon.com/making-a-case-for-domain-modeling-17cf47030732)
* `CRUD`
  * Functions of Persistent Storage: Create, Read, Update, Delete
    * [stackify](https://stackify.com/what-are-crud-operations/)
* `schema`
  * a skeleton structure representative of the logical view of an entire database
    * [tutorials point](https://www.tutorialspoint.com/dbms/dbms_data_schemas.htm)
* `sanitize`
  * the process of removing data with the purpose of making it unrecoverable
  * generally used to protect systens from malicious data
    * [medium](https://medium.com/@abderrahman.hamila/what-sanitize-mean-and-why-sanitize-in-code-data-5c68c9f76164)
* `Structured Query Language (SQL)`
  * the standard language for relational database management
    * [sqlcourse](http://www.sqlcourse.com/intro.html)
* `Non SQL (NoSQL)`
  * non-relational databases which provide flexible schemas, scale easily, and can handle large amounts of data and high user loads
    * [mongodb](https://www.mongodb.com/nosql-explained)
* `MongoDB`
  * a NoQL document-oriented database program
    * [mongodb](https://www.mongodb.com/)
* `Mongoose`
  * an object modeling tool designed for use with MongoDB
    * [freecodecamp](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)
* `record`
  * a basic data structure composed of collections of elements
    * [wiki](https://en.wikipedia.org/wiki/Record_(computer_science))
* `document`
  * JSON data stored in a database 
    * [mongodb](https://www.mongodb.com/document-databases)
* `Object Relation Mapping (ORM)`
  * a programming technique for bridging between objects and tables
  * ORM libraries take care of the bridging mechanics and
  * allow the user to interact directly with the objects in the user's preferred language
    * [stackoverflow](https://stackoverflow.com/questions/1279613/what-is-an-orm-how-does-it-work-and-how-should-i-use-one)
