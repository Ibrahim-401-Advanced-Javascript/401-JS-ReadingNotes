### Week 7

***

#### Class 31

##### Hooks API
* Why do we not need more .html pages in a multi-page React app?
  * We can store components within components within the app and use pagination to switch between views
* If we wanted a component to show up on every page, where would we put it and why?
  * Inside a `<Route />`
 
##### Vocabulary
* `children / child components`
  * the components nested within another component
* `hash routing`
  * utilizing routes marked with `#` instead of `/` in order to build single-page applications
  * the `#` targets a specific component or section on the page and loads it or focuses on it
* `link routing`
  * using traditional external or local routes, marked with `/`
  * allows us to navigate between components on different pages within the application
    
***

#### Class 32

##### Custom Hooks
* What does a component's life cycle refer to?
  * the runtime associated with and the resources utilized by the component
* Why do you sometimes need to wrap functions in `useCallback` when called from within `useEffect`?
  * to prevent the recreation of functions
  * if a function is called inside of a `useEffect` function and we don't want it to be re-created after every render cycle
    * [medium](https://medium.com/@infinitypaul/reactjs-useeffect-usecallback-simplified-91e69fb0e7a3)
* Why are functional components preferred over class components?
  * they are lightweight (less code), easier to test, and future React versions will likely performance boost functional components
 
##### Vocabulary
* `state hook`
  * allows us to add state to functional components
    * [reactjs](https://reactjs.org/docs/hooks-state.html)
* `effect hook`
  * allows us to handle side effects of functional components
  * runs after every render cycle
  * allows us to register functions which will execute after the current render cycle
    * [medium](https://medium.com/@infinitypaul/reactjs-useeffect-usecallback-simplified-91e69fb0e7a3)
* `reducer hook`
  * allows us to use state when the next state depends on the previous one
    * [reactjs](https://reactjs.org/docs/hooks-reference.html#usereducer)
    
***

#### Class 33

##### Context API
* Describe use cases for `useMemo()` and `useReducer()`
  * useMemo is helpful when you have a list and you don't want it to be initialized on every render, rather you want to just add to it and retrieve values only when necessary
  * useReducer is helpful when the next state relies heavily on the previous one
   * it is similar to useState but preferable in this instance. 
   * i.e. incrementing counts
* Why do custom hooks need the use prefix?
  * to identify them as hooks rather than standard functions wherever they are imported
  * to follow React naming conventions
* What do custom hooks usually do?
  * perform functions that you want to use across components without repeating code in each component
* Describe how a hook that fetches API data might work
  * awaits a data fetch
  * returns the data object
  * returning the data returned by the hook in any given component will allow you to manipulate and populate it in whatever way is appropriate for that specific component
 
##### Vocabulary
* `reducer`
  * a function which takes two arguments: current state and action to perform on the state
  * returns a new state
    * [robinwieruch.de](https://www.robinwieruch.de/javascript-reducer)

***

#### Class 34

##### Login & Auth
* Why is the Context API useful?
  * a
* Can a component outside of a provider get its context?
  * a
* What are some common use cases for using the Context API?
  * a
* Describe 'Context Hell'
  * a
 
##### Vocabulary
* `global state`
  * def
    * [src](url)
* `global context`
  * def
    * [src](url)
* `provider`
  * def
    * [src](url)
* `consumer`
  * def
    * [src](url)
    
***

#### Class 35

##### Graphs
* Concept
  * description

##### Vocabulary
* `term`
  * def
    * [src](url)
