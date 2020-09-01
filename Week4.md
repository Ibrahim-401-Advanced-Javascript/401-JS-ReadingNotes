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

