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
  * answ
* When a component “wraps” another component, how does the child component’s output get rendered?
  * answ
* Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?
  * answ
* What trick can a parent use to share all props with it’s children
  * answ
 
##### Vocabulary
* `props.children`
  * def
    * [src](url)
* `composition`
  * def
    * [src](url)

***

#### Class 30

##### Hash Tables
