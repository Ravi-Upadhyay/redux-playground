# Redux

> React is a state management library which makes creating complex web application easier. It aims to solve problem of state update and it's propagation. It provides a deterministic way to do the state update. It empowers us with extra control.

- Thus, we can have more information about when, why and how about the state updates.
- Redux devtools, help us to make development, testing and debugging lot easier.
___

## Index

- [Philosophy of Redux](#philosophy)
- [Tips & Tricks](#tips)
- [Code snippets](#code-snippets)
- [Resources over web](#resources)
- [To do list](#to-do)

___

## Philosophy of Redux<a name="philosophy"></a>

### Need of Redux (The problem statement):

- As the requirements for JavaScript` single-page applications` have become increasingly complicated, our code must manage more `state` than ever before.
- At some point, you no longer understand what happens in your app as you have lost control over the when, why, and how of its `state`.
- When a system is opaque and non-deterministic, it's hard to reproduce bugs or add new features.

### The three principles (The solution):

- **Single source of truth:** The `state` of your whole application is stored in an object tree within a single `store`.
- **State is read-only:**  The only way to change the `state` is to emit an `action`. This ensures that neither the `views` nor the `network callbacks` will ever write directly to the `state`. Instead, they express an intent to transform the `state`.
- **Changes are made with pure functions:** To specify how the `state` tree is transformed by actions, you write pure `reducers`.

### The redux cycle: 

The philosophy of redux can finally be understood by this flow where redux used the three principles described above to create a state management utility.

![Redux Flow](resources/redux-flow.jpg)

#### Action Creators: 

Action creators are exactly that—functions that create actions. It's easy to conflate the terms `action` and `action creator`, so do your best to use the proper term.

In `Redux`, `action creator`s simply return an `action`:

```javascript

/*EXAMPLE: A simple action creator*/
function addTodo(text) {
  return {
    type: ADD_TODO,
    text
  }
}

```

#### Actions:

Actions are payloads of information that send data from your application to your `store`. They are the only source of information for the `store`. You send them to the `store` using `store.dispatch()`.

Actions must have a `type` property that indicates the type of action being performed.

```javascript

/*EXAMPLE: A simple action*/
const ADD_TODO = 'ADD_TODO'

{
  type: ADD_TODO,
  text: 'Build my first Redux app'
}

```

#### Reducers:

Reducers specify how the application's `state` changes in response to actions sent to the `store`. Remember that actions only describe what happened, but don't describe how the application's state changes.

The `reducer` is a pure function that takes the `previous state` and an `action`, and returns the `next state`.

_Given the same arguments, it should calculate the next state and return it. No surprises. No side effects. No API calls. No mutations. Just a calculation._

_It's important to return the previous state for any unknown action._

```javascript

/*EXAMPLE: A simple reducer*/
function todoApp(state, action) {
  if (typeof state === 'undefined') {
    return initialState
  }

  // For now, don't handle any actions
  // and just return the state given to us.
  return state
}

```



### Whether to use Redux or not:

Redux is a valuable tool for managing the state, but this also has certain trade offs. One should always take time and consider according to the needs. Although these guides are subjective and vague. 

- You have reasonable amounts of data changing over time.
- You need a single source of truth for your state.
- You find that keeping all your state in a top-level component is no longer sufficient.
___

## Tips & Tricks<a name="tips"></a>

1. In Redux, all the application state is stored as a single object. It's a good idea to think of its shape before writing any code. What's the minimal representation of your app's state as an object?
2. You'll often find that you need to store some data, as well as some UI state, in the state tree. This is fine, but try to keep the data separate from the UI state.
3. In a more complex app, you're going to want different entities to reference each other. We suggest that you keep your state as normalized as possible, without any nesting. Keep every entity in an object stored with an ID as a key, and use IDs to reference it from other entities, or lists. Think of the app's state as a database. This approach is described in normalizr's documentation in detail. For example, keeping todosById: { id -> todo } and todos: array\<id\> inside the state would be a better idea in a real app, but we're keeping the example simple.

___

## Code Snippets<a name="code-snippets"></a>

1. <!-- link to code snippets -->

___

## Resources over web<a name="resources"></a>

1. [Redux official](https://redux.js.org/introduction/getting-started)
2. [Redux starter kit - opinionated](https://redux-starter-kit.js.org/)
3. [Redux devtools](https://github.com/reduxjs/redux-devtools)
4. [Redux video tutorial, Dan Abramov - Creator of Redux](https://egghead.io/courses/getting-started-with-redux)
5. [Redux video tutorial, Dan Abramov - Creator of Redux (Advanced)](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)
6. [Redux Fundamentals, Mark - Co-maintainer of Redux](https://blog.isquaredsoftware.com/2018/03/presentation-reactathon-redux-fundamentals/)
7. [Redux Fundamentals, Mark - Co-maintainer of Redux (Advanced)](https://blog.isquaredsoftware.com/series/practical-redux/)
8. [React-Redux - Official bindings for react redux](https://react-redux.js.org/)
   

___

## To do list<a name="to-do"></a>

1. ~~Top most section Redux needs to be updated as definition and objectives become more clear.~~
2. Follow tutorials of Dan and Mark, mentioned in resources over web,
3. Do some coding and POC
4. Read in detail: section - Note on switch and boilerplate (https://redux.js.org/basics/reducers)