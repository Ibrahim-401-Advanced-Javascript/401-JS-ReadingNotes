### Week 6

***

#### Class 26

##### Component Based UI
* Name 5 Javascript UI Frameworks (other than React)
  * Angular
  * Ember
  * Backbone
  * Vue
  * Aurelia
* What’s the difference between a framework and a library?
  * libraries contain functions that an app can call to perform tasks while frameworks utilize functions to design and build the interface
 
##### Vocabulary
* `Rendering`
  * the process of generating data
* `Templates`
  * sample documents which can be added to, modified, or completed in order to build a unique application
  * starter code
* `State`
  * the current status of a system which can be changed over runtime
    
***

#### Class 27

##### Props and State
* Does a deployed React application require a server?
  * No, you instead you run `npm run build`
* What does npm run build do?
  * Bundles and minifies dependencies, javascript code, and css
* Why do we prefer to test a React application at the behavior rather than the unit level?
  * By running behavior-driven tests, we can assess that our code is doing what we want it to do, given the appropriate state. 
  * Outcomes will be state-specific so it's important to test a given state and a changed state. 
* Describe the actual composition / architecture of a React application
 
##### Vocabulary
* `BDD`
  * Behavior Driven Development
  * Tests outcomes given particular states
    * [codeburst.io](https://codeburst.io/react-behavior-driven-development-bdd-535afd364e5f)
* `Acceptance Tests`
  * A pass-or-fail test of the behaviors of an application
  * Frequently automated
    * [agile alliance](https://www.agilealliance.org/glossary/acceptance/)
* `Mounting`
  * the process of creation and insertion into the DOM
    * [reactjs](https://reactjs.org/docs/react-component.html)
    
***

#### Class 28

##### Component Composition
* Can a parent component access the state of a child component?
  * No, but parent and child components can pass data to one another in order to update local states.
  * Child components can access the state of a parent component if the parent passes its state to the child.
  * State data only flows downward in this way.
* What can be passed along in a prop variable?
  * Functions or Bits of data used to update states
* How can a child component “know” the state of another component?
  * If the other component passes data to the parent in order for the parent to update state, and the parent passes its state along to another child
 
##### Vocabulary
* `component props`
  * property objects or functions which belong to components and can be passed to parent and child components
* `component state`
  * 'what's going on right now' for each component
  * the current status of any given component in its run process
* `application state`
  * same concept as component state, but on an app-wide level
  * the state of the highest-level parent component
    
***

#### Class 29

##### Routing
* Do child components have direct access to props/state from the parent?
  * It depends on what is meant by 'direct.' They have the ability to have direct access, but they need to be passed in via props before access is readily available. 
* When a component “wraps” another component, how does the child component’s output get rendered?
  * Using a router
* Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?
  * Yes
* What trick can a parent use to share all props with it’s children
  * by passing in any props to the `<Component />` tag, they become available to any component with them linked in.
 
##### Vocabulary
* `props.children`
  * used to display whatever you include between the opening and closing tags when invoking a component
    * [codeburst.io](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)
* `composition`
  * the process of creating generic child components which will later become more specialized with props
    * [reactjs](https://reactjs.org/docs/composition-vs-inheritance.html)

***

#### Class 30

##### Hash Tables
* Hashtables are used to hold unique values. They can be used as a virtual dictionary or library
* They contain nodes (buckets) which contain a key and a value
* They are essentially arrays which contain small objects which contain key value pairs.
* We use them because of the efficient ability of arrays to quickly locate any value, given its index.
  * When a value is stored, its hash key is assigned a specific index so that we can do this

##### Vocabulary
* `hash`
  * a key created as a result of an algorithm converting a datastring into a scrambled mix of characters
  * used for security or unique variables
* `buckets`
  * the storage space at each index of a hash table
  * each index is one bucket
* `collisions`
  * when more than one key gets hashed and assigned to the same bucket of the hash table
