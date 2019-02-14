# Redux

> React is a state management library which makes creating complex web application easier. It aims to solve problem of state update and it's propagation. It provides a deterministic way to do the state update. It empowers us with extra control.

- Thus, we can have more information about when, why and how about the state updates.
- Redux devtools, help us to make development, testing and debugging lot easier.
___

## Index

- [Philosophy of Redux](#philosophy)
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

### Whether to use Redux or not:

Redux is a valuable tool for managing the state, but this also has certain trade offs. One should always take time and consider according to the needs. Although these guides are subjective and vague. 

- You have reasonable amounts of data changing over time.
- You need a single source of truth for your state.
- You find that keeping all your state in a top-level component is no longer sufficient.
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
   

___

## To do list<a name="to-do"></a>

1. ~~Top most section Redux needs to be updated as definition and objectives become more clear.~~
2. Follow tutorials of Dan and Mark, mentioned in resources over web,
3. Do some coding and POC