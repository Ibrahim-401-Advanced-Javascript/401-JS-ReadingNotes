### Week 8

***

#### Class 36

##### Redux - Application State
* What are the advantages of storing tokens in “Cookies” vs “Local Storage”
  * persistence of storage without re-logging in, persistence until manual deletion, greater amount of storage capacity
* Explain 3rd party cookies.
  * cookies that are set by a website other than the website you are on
  * i.e. facebook like buttons on sites outside of facebook, advertisement services that monitor which sites are visited by the user
* How do pixel tags work?
  * pixel tags are 1×1-pixel graphics used for tracking user behavior and web traffic at a site’s server level
  * they allow companies to track events, email opens, digital ad impressions, sales conversions, website visits, and other types of web activity
  * tracking pixels are added using a code in the site’s HTML code or email, which contains an external link to the pixel server. When someone visits a website using a tracking pixel, the HTML code is processed by their browser, which follows the link and opens the hidden graphic. This action is identified and recorded in the server’s log files
  * when a user opens an email, visits a website, views your digital ad, or takes any other action, they are actually requesting the server to download the tracking pixel attached to the content
    * [whatagraph](https://whatagraph.com/blog/articles/tracking-pixel)
 
##### Vocabulary
* `cookies`
  * small pieces of information websites store on your computer
  * only contain bits of text, i.e. a user ID, session ID, preferences/settings
  * function as user-specific memory that persists across web sessions until being cleared
* `authorization`
  * the process of defining what a user has access to
  * including abilities related to data, i.e. read-only, adding, editing, deleting content
* `access control`
  * a means of verifying user identity and verifying that a user has appropriate control over data
* `conditional rendering`
  * creating components that encapsulate the data you want to show based on whether a given condition is met
  * using conditional statements to render only those components you want to show when the application is in the appropriate state
    
***

#### Class 37

##### Redux - Combined Reducers
* Why choose Redux instead of the Context API for global state?
  * when we need to perform changes to state behind the scenes which will determine how the application renders
  * (versus using context api to perform those changes on the component where the state will be rendered directly)
* What is the purpose of a reducer?
  * to determine changes to an application's state
* What does an action contain?
  * an action is a function which takes in a value (often a value of an object or a deconstructed object) and returns an object with the type of action to perform and the payload (generally, what was passed into the function as the argument)
* Why do we need to copy the state in a reducer?
  * it is important to not directly mutate/manipulate state

##### Vocabulary
* `immutable state`
  * cannot be modified after it is created
* `time travel`
  * the process of using reducer methods to capture states at any given time and move back and forth between those states 
    * [front-end armory](https://frontarm.com/swyx/reusable-time-travel-react-hooks-immer/)
* `action creator`
  * functions that create actions
* `reducer`
  * a function which determines changes to an application's state
* `dispatch`
  * a function which assists in passing actions to components
    
***

#### Class 38

##### Redux - Asynchronous Actions
* How granular should your reducers be?
  * It depends on how much of the properties in state any component cares about at a given time
  * In other words, if you want to update only one property in state, but the application cares about the entire state object, it could be tempting to update all properties of the state object at once
  * However, we can perform an action on specific fields and still update the entire object
  * Reducers should be grouped together based on the shape of the state object at any given time, as well as how frequently it will change, etc.
  * If it makes sense to separate portions of the state into their own reducers, do it. If not, don't.
* Multiple reducers can “fire” when a commonly named action is dispatched. Is this a Pro or Con?
  * Pro if intentional, Con if not.
* Name a strategy for preventing the above
  * Name actions meaningfully while keeping this feature in mind

##### Vocabulary
* `store`
  * holds the state of the application
  * performs actions on the state and dispatches those actions to components
* `combined reducers`
  * more than one function performing actions on separate state components, gathered in one store.js file
    
***

#### Class 39

##### Redux - Asynchronous Actions
* What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
* When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

##### Vocabulary
* `middleware`
  * def
    * [src](url)
* `thunk`
  * def
    * [src](url)
