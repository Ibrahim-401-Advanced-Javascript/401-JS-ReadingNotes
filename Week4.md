### Week 4

***

#### Class 16

##### Access Control
* Why is access control important?
  * We don't want to give every user who logs in the same capabilities. For example, some users would have administrative privileges, others would have the ability to edit content, and some would simply have read-only access.
* Describe an application that would need access control.
  * Blogs or other Publications, Government Agencies, Financial Institutions
  * Essentially anything with potentially sensitive information attached
* What is a role used for?
  * To define a user's capabilities as they relate to data within an application
* Why is role based access control more scalable than discretionary or mandatory access control?
  * Mandatory Access Control is strictly enforced by one system administrator and requires a great deal of planning before implementation; there is also a high system management overhead associated with constantly updating object and account labels, as these things must change to accomodate new data and new users, as well as changes to categories and classification of existing users. As the user base grows, this practice becomes less scalable because of the high level of autonomy each user has over its own data.
  * Discretionary Access Control is enforced by the operating system (under control of a system administrator). It is categorized by the user's ability to control access to their own data. 
  * Role Based Access Control assigns permissions to particular roles within an organization. Users, upon signup, are assigned to that particular role. This is the most scalable because there are no deviations from this rule. One user will never have more capabilities than another user, and one editor will never have more capabilities than another editor. By creating roles first, it is ensured that no matter how many users of any type are added, their permissions are granted in the same way and there don't need to be changes to the code.
    * [techtopia](https://www.techotopia.com/index.php/Mandatory,_Discretionary,_Role_and_Rule_Based_Access_Control)

***

#### Class 17

##### TCP Servers
* Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?
 * HTTP method calls and data retrievals/creations, timers
* Why are events sometimes better than asynchronous actions with callbacks?
 * faster server response time (all happens synchronously)
 * can respond to the same event signal multiple times without needing to write extended logic for this within the function
* What does an EventEmitter instance do?
 * starts events upon specific conditions
 * calls listener functions
* When is a program’s call stack, event queue, and event loop active?
 * while the code is being invoked / read by the interpreter
 
##### Vocabulary
* `Observer Pattern`
  * a one-to-many dependency between objects
  * when the object changes state, all dependents are updated automatically
    * [geeksforgeeks](https://www.geeksforgeeks.org/observer-pattern-set-1-introduction/)
* `Listener`
  * a function that will run when its target is hit
  * it literally "listens" for an event
* `Event Handler`
  * the function which runs when the event listener detects the event has been triggered
* `Event Driven Programming`
  * a programming paradigm in which the flow of execution is determined by events
    * [freecodecamp](https://www.freecodecamp.org/news/understanding-node-js-event-driven-architecture-223292fcbc2d/)
* `Event Loop`
  * monitors the call stack and the callback queue
  * takes the first event from the queue and pushes it to the call stack, which runs it
* `Emit/Raise/Trigger`
  * Event emitter emits an event - that is it enacts the code upon being triggered by the listener
* `Subscribe`
  * the listener is 'subscribed' to event objects; when the event object is triggered, the listener reacts by enacting the event handler or emitter

***

#### Class 18

##### Socket.io
* What is the benefit of transforming data into packets?
  * packet-based networks are the most scalable and efficient networks for content delivery
    * [fnt software](https://blog.fntsoftware.com/network-transformation-transitioning-to-packet-technology/)
* UDP is often refereed to as a connectionless protocol. Why is this?
  * no connection needs to be established between source and destination prior to the transmission of data
    * [wikipedia](https://en.wikipedia.org/wiki/Connectionless_communication)
* Can a socket server application have multiple socket connections?
  * Yes, a socket server may serve many clients
* Can a socket connection application be connected to multiple socket servers?
  * Yes, a socket application can utilize numerous servers
* Can an application be both a socket server and a socket connection?
  * No, each socket application has servers which have connections, but one cannot be both.

##### Vocabulary
* `OSI Model`
  * Open Systems Interconnection Model
  * a conceptual model of the layers of systems communication
    * application layer : human-computer interaction
    * presentation layer : ensures data is in usable format and is encrytpted
    * session layer : maintains connections & controls ports
    * transport layer : transmits data
    * network layer : decides which path data will take
    * datalink layer : defines the format of data
    * physical layer : transmits raw bit stream 
      * [cloudflare](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
* `TCP Model`
  * Transition Control Protocol Model
  * a concise version of the OSI model with stricter boundaries
    * application layer : performs the functions of OSI's application, presentation, and session layers
    * transport (host-to-host) layer : TCP occurs here (see definition below)
    * internet layer : analogous to OSI's network layer
    * network access layer : combination of OSI's physical and datalink layer
      * [geeksforgeeks](https://www.geeksforgeeks.org/tcp-ip-model/)
* `TCP`
  * Transition Control Protocol
  * a connection-oriented protocol for data transmission/exchange
  * a connection is established and maintained until each entity has finished transmitting data
    * [techtarget](https://searchnetworking.techtarget.com/definition/TCP)
* `UDP`
  * User Datagram Protocol
  * a connectionless protocol for data transmission/exchange
  * less reliable than TCP
* `Packets`
  * small amounts of data sent over a network, including a source, destination, and content
* `Socket`
  * a software structure that serves as an endpoint for transmitting and receiving data across a network
  
***

#### Class 19

##### Message Queues
* What does it mean that web sockets are bidirectional? Why is this useful?
* Does socket.io use HTTP? Why?
* What happens when a client emits an event?
* What happens when a server emits an event?
* What happens if a client “misses” an event?
* How can we mitigate this?

##### Vocabulary
* `Term`
  * def
    * [src](url)
* `Web Socket`
  * def
    * [src](url)
* `Socket.io`
  * def
    * [src](url)
* `Client`
  * def
    * [src](url)
* `Server`
  * def
    * [src](url)
