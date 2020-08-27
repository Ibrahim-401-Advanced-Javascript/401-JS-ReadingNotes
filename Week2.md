### Week 2

***

#### Class-06

##### HTTP and REST

* HTTP (Hyper Text Transfer Protocol)
  * Apps built using HTTP subscribe to the cient-server computing model
    * server = host designed to provide the service
    * client = hosts that make requests to the service
  * HTTP Requests
    * GET method -> retrieve a resource
    * HEAD -> retrieve headers
    * POST -> create a resource
    * PUT -> update a resource by replacing it
    * DELETE -> delete a resource
    * CONNECT -> create a TCP/IP tunnel (communicate between 2 networks)
    * OPTIONS -> returns supported methods for a URL
    * TRACE -> echos retrieved request (used for debugging)
    * PATCH -> modify specific parts of a resource
      * [mdn](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
  * HTTP Response
    * First line contains HTTP Version (i.e. HTTP/1.1), Status Code (i.e. 200), and Status Message(i.e. 'OK')

* REST (Representational State Transfer)
  * REST Methods allow us to perform actions on data returned from RESTful API calls
    * CREATE -> Create a new record
      * like HTTP POST
    * READ -> Retrieve records
      * like HTTP GET
    * UPDATE
      * like HTTP PUT or PATCH
    * DELETE -> Remove a record

***

#### Class-07

##### Express MiddleWare

* Functions that requests are routed through
* Receive a request object, response object, and the next middleware function in the req/res cycle
  * if the function doesn't end the req/res cycle, it must call next() or the request will run for ever and ever and ever and ever and-
* order matters (a lot) when coding middleware functions
* application middleware handles:
  * errors
  * importing other routes
  * applying defaults
  * parsing
* route middleware handles:
  * logging
  * model loading
  * browser/location/user specific content
  * pre-rendering
* built-in middleware functions include:
  * express.static -> serves static assets such as HTML files, images, etc.
  * express.json -> parses incoming requests with JSON payloads
  * express.urlencoded -> parses incoming requests with URL-encoded payloads
  * [express](https://expressjs.com/en/guide/using-middleware.html#middleware.built-in)
    
***

#### Class-08
 
##### Express Routing
* Router is essentially a mini express application
  * It provides us with routing APIs:
    * .use
    * .get
    * .param
    * route
  * Basic routes include simple page routing with callback functions
  * Route middleware includes functions we want to run before information is loaded to the user:
    * logging
    * pre-rendering
    * user authentication
  * Routes with parameters (i.e. '/route/:parameter') send or populate data that is specific to a parameter value
    * parameters are validated using .param()
* Route functions take two mandatory arguments: request, response
  * Request Objects can take parameters or query strings
  * Response Object is responsible for sending data back to the browser
    * sends status code
    * sends data objects

***

#### Class-09
 
##### Sub Documents in Mongoose
* Subdocuments are documents embedded in other documents; they come in two types:
  * arrays of subdocuments
  * arrays of subdocuments
* They enable us to nest schemas within other schemas 
* Nested schemas can have middleware, validation, and any other feature normally accessible to schemas
* However, subdocuments are not saved on their own; they are only saved whenever their parent document is saved
* [mongoose](https://mongoosejs.com/docs/subdocs.html)

##### Joining Documents in Mongo
* Virtual Joins
  * `const Schema1 = new Schema({})`
  * `const Schema2 = new Schema({})`
  * `------`
  * `Schema2.virtual('items', { ref: 'Model1 }`
  * `------`
  * `const Model1 = mongoose.model('Model1', Schema1)`
  * `const Model2 = mongoose.model('Model2', Schema2)`
  * `------`
  * By making reference to the model we want to link our schema to, we can join them. 
* [mongoose](https://mongoosejs.com/docs/populate.html#populate-virtuals]

***

#### Class-10

##### Stacks
* Stacks are structures that consist of nodes
* When referencing actions performed on stacks, we use the following terms:
  * Push -> items added into the stack are pushed (like arrays)
  * Pop -> items removed from the stack are popped (like arrays)
  * Top -> this is the top node in the stack
  * Peek -> peeking gives you the value of the top node in the stack
  * isEmpty -> returns true when the stack is empty, else returns false
* Stacks follow FILO and LIFO concepts
  * FILO -> first in/last out -> the first item added to the stack will be the last one popped out
  * LIFO -> last in/first out -> the last item added to the stack will be the first one popped out
  
##### Queues
* Queue Vocab
  * Enqueue -> Nodes that are added to the queue
  * Dequeue -> Nodes that are removed from the queue
  * Front -> The first Node of the queue
  * Rear -> The last Node of the queue
  * Peek -> gives you the value of the front Node in the queue
  * IsEmpty -> returns true when the queue is empty, else false
* Queues also follow FIFO and LILO concepts
  * FIFO -> first in first out -> first item in the queue will be the first item out of the queue
  * LILO -> last in last out -> last item in the queue will be the last item out of the queue
 
