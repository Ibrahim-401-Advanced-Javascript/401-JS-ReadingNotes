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
  * a
* Why do custom hooks n eed the use prefix?
  * a
* What do custom hooks usually do?
  * a
* Using any list of custom hooks, research and name one that you think will be useful in your applications
  * a
* Describe how a hook that fetches API data might work
  * a
 
##### Vocabulary
* `reducer`
  * def
    * [src](url)

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
