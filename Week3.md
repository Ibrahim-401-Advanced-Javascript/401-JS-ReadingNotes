### Week 3

***

#### Class 11

##### Authentication
* Router Middleware
  * Middleware functions have access to the request object, response object, and the next middleware function in the web request-response cycle
  * Middleware functions can:
    * execute any code
    * make changes to the request and/or response objects
    * end the request-response cycle
    * call the next middleware function in the stack
  * Express apps can use:
    * application-level middleware - `app.httpmethod(function)` or `app.use(function)`
    * router-level middleware - `const router = express.Router` -> `router.use(function)` or `router.httpmethod(function)`
    * error-handling middleware - `app.use(function(err, req, res, next)`
      * takes four arguments; in addition to req, res, next, we add err
    * built-in middleware
      * `express.static` serves static assets such as HTML files and images
      * `express.json` parses requests with JSON payloads
      * `express.urlencoded` parses incoming requests with url-encoded payloads
    * third-party middleware
      * dependencies that we install with node which add specific functionalities to express applications
* Dynamic Module Loading
  * wrapping imports in async functions
  `async function loadPage() { await import('file/path/filename.js); code to run after completion of import goes here }`
    *[github](https://gist.github.com/Rich-Harris/ea561810900eedd2a8e9afbc78ddd566)
* Singleton Pattern
  * The Singleton Pattern involves a single class responsible for creating an object while ensuring that only a single object gets created
  * The object can be accessed directly without needing to instantiate the object class, as it has been automatically instantiated upon its creation
    * [tutorialspoint](https://www.tutorialspoint.com/design_pattern/singleton_pattern.htm)
* CRUD -> REST Method Matches
  * Create - POST
  * Read - GET
  * Update - PUT
  * Delete - DELETE
* Mock Testing
  * Mock functions allow us to test code by 'erasing' the actual implementation of the function, instead creating mock situations to base our code connection tests on. 

***

#### Class 12
 
##### OAuth
* Why is authentication important?
  * Protecting a user's private or sensitive information
* Why should we be careful about storing users' passwords?
  * Data breaches occur often, and if we are not careful about the information we store along with encrypted passwords, we could be giving hints to how to easily decrypt them. 
* What is the difference between hashing and encryption?
  * Hashing is a one-way irreversible data conversion using alphanumeric characters to produce a new key, a complex string of letters and numbers
  * Encryption is a secure encoding technique in which data is encoded using an algorithm which only authorized personnel have access to
    * [geeksforgeeks](https://www.geeksforgeeks.org/encryption-encoding-hashing/)
* What is the difference between encryption and encoding?
  * Encoding is the reversible process of changing data into a new format 
  * Encryption is a secure encoding technique (see above)
    * [geeksforgeeks](https://www.geeksforgeeks.org/encryption-encoding-hashing/)
* What is a token used for?
  * Secure information transmission
  * Persistence of user authorization

##### Vocabulary
* `authentication`
  * the verification of human-server transfer of credentials 
* `authorization`
  * the validation of which functions of an application the user has access to
    * [medium](https://medium.com/capital-one-tech/securing-applications-with-better-user-authorization-625ec07a7001)
* `session`
  * characterized as a temporary interactive information exchange between two web clients, or between a web client and a user
    * [wikipedia](https://en.wikipedia.org/wiki/Session_(computer_science))
* `cookie`
  * small bits of data stored by browsers which track stateful information (i.e. browsing activity, logins, clicks, shopping carts)
* `token`
  * a complex string of base64 characters which is granted to the user after authentication and authorization
    * [jwt.io](https://jwt.io/introduction/)
* `basic auth`
  * the simplest auth technique, which encodes data with base64
  * generally combined with HTTPS to provide confidentiality of data
    * [swagger.io](https://swagger.io/docs/specification/authentication/basic-authentication/)
* `secret`
  * a key used in conjunction with a client id to be used for OAuth
* `cryptography`
  * the study and practice of secure communications techniques which allow only the sender and intended recipient to view sent data
    * [kaspersky](https://usa.kaspersky.com/resource-center/definitions/what-is-cryptography)

***

#### Class 13

##### Bearer Authorization
* Write the following steps in the correct order:
  1. Register your application to get a client_id and client_secret
  2. Make a request to a third-party API endpoint
  3. Ask the client if they want to sign in via a third party
  4. Redirect to a third party authentication endpoint
  5. Receive authorization code
  6. Make a request to the access token endpoint
  7. Receive access token
* What can you do with an authorization code?
  * Obtain an access token
* What can you do with an access token?
  * Implement single-sign-in functionality & persistent authorization
* What’s a benefit of using OAuth instead of your own basic authentication?
  * Single-sign-on systems give the user one less password to worry about managing. Additionally, it grants user more control over their data; they control which applications have what type of access to which type of data.
  
##### Vocabulary
* `Client ID`
   * a public identifier for applications
   * generally not easily guessable
      * [oauth2.0](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
* `Client Secret`
   * a string known only to the application & the authorization server
      * [oauth2.0](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)
* `Authorization Endpoint`
   * a route used to interact with the resource owner and get the authorization to access the secure resource
      * [auth0](https://auth0.com/docs/protocols/protocol-oauth2)
* `Access Token Endpoint`
   * a route used by the application in order to get an access token or a refresh token
      * [auth0](https://auth0.com/docs/protocols/protocol-oauth2)
* `API Endpoint`
   * a route used as a point of entry when two systems (client-server) are interacting
   * the means from which the API can access the resources they need from a server to perform their task
      * [rapidapi](https://rapidapi.com/blog/api-glossary/endpoint/)
      
***

#### Class 14

##### Access Control (ACL)
* When is Basic Authorization used vs. Bearer Authorization?
  * Basic Authorization involves a base64-encoded username and password being proided to the browser, checked against a database of sorts, and granting access if the provided user:pass pair matches the databased user:pass combination 
  * Bearer Authentication uses a token, which is a cryptic string, to grant access to the authorized user.
    * [swagger.io](https://swagger.io/docs/specification/authentication/bearer-authentication/)
* What does the JSON Web Token package do?
  * It connects authorization headers, a payload with user info and other data, and a secret to form an encoded string, with each of the aforementioned parts being separated by a '.' This is the token.
* What considerations should we make when creating and storing a SECRET?
  * The secret should be moderately complex and not easily guessable; it should also not contain any sensitive information about the user

***

#### Class 15

##### Binary Trees
* Binary Trees are a data structure composed of nodes. Like a linked list, stack, or queue, binary trees have traversal alrogithms associated with them and a few different means of traversal.
  * Depth First Traversal entails going through the tree from root(the highest parent node) to the leaves(last child nodes) or vice versa. Within depth first traversal, there are some different options:
    * Pre-order traversal moves from root to left to right
    * In-order moves from left to root to right
    * Post-order moves from left to right to root
  * Breadth First Traversal involves going through each level of the tree node-by node (level-by-level, left to right like reading a page of text).
    * A queue is used to perform this process
* A node within a binary tree has three properties:
  * The value that is stored in the node
  * A reference to the node to its left
  * A reference to the node to its right

##### Binary Search Trees
* Binary Search Trees are more structured than Binary Trees, whose nodes can be arranged in any order
  * Binary Search trees must be sorted as such:
    * All nodes smaller than the root node are placed to the left of the root
    * All nodes larger than the root node are placed to the right of the root
    * This principle is followed for each parent node in the tree; a node's left child is always smaller, while a node's right child is always larger.
* Binary Search Trees can be traversed using a similar method to binary search
  * Starting at the root, we can simply check whether the value of the node is smaller or larger than the value we are searching for (or seeking to add)
  * If the value is smaller than the root, we move left and repeat the process (using a while loop is best practice)
  * If the value is larger than the root, we move right and repeat, as above. 
  * We repeat this process until we find the node with the value we are looking for, or find it's proper place if we are trying to add a new node
