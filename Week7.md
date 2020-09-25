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
  * it allows us to pass properties between components without having to call props within each component
* Can a component outside of a provider get its context?
  * no
* What are some common use cases for using the Context API?
  * when an application requires the same logic be used within numerous components
* Describe 'Context Hell'
  * when there are many nested components within one application which need to share functions/state
 
##### Vocabulary
* `global state`
  * the practice of holding an application's state properties within the highest parent and allowing access to all child components
* `provider`
  * the component that creates/manipulates and exports the data needed by other components
* `consumer`
  * the component that receives state information (or whatever data is passed by the provider)
    
***

#### Class 35

##### Graphs
* Concept
  * a series of vertices (nodes) connected by edges
* Traversal
  * similar to breadth-first tree traversal
  * exception: graphs can have cycles
    * to prevent an infinite loop, we set a flag to indicate whether that vertex has already been accessed
* Breadth-First Review:
  * enqueue declared start node into the queue
  * loop while there are still nodes present
  * dequeue the first node from the queue
  * if the dequeued node has unvisited child nodes, mark them as visited and reinsert them in the queue

##### Vocabulary
* `vertex`
  * a data object, essentially a node
  * can have zero or more adjacent vertices (neighbors)
* `edge`
  * the connection between two vertices
* `neighbor`
  * vertices connected to another via edges
  * a.k.a. adjacent vertices
* `degree`
  * a vertex property
  * the number of edges connected to that vertex
* `adjacency matrix`
  * a two-dimensional array
  * if there are n vertices, the graph is represented by an n x n matrix
  * each row and column represents each vertex of the data structure
  * the values within the inner arrays are integers which represent the number of connections between vertex row and vertex column
* `adjacency list`
  * a collection of linked lists that lists all other vertices which are connected to each particular vertex
* `undirected graph`
  * edges are undirected or bi-derectional
  * data does not flow in one specific direction
* `diagraph`
  * edges are directed
  * each vertex is directed at another vertex with a specific requirement about which vertex should be referenced next
  * a.k.a. directed graph
* `cyclic graph`
  * a directed graph that starts and ends with the same vertex
* `acyclic graph`
  * a directed graph without cycles
  * trees are one form of acyclic graphs
* `complete graph`
  * all vertices are connected to all other vertices
* `connected graph`
  * all vertices have at least one edge
  * trees are one form of connected graphs
* `disconnected graph`
  * some vertices may not have any edges

* `weighted graph`
  * def
