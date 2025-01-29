# ContexAPI + useReducer

- built-in react (no need to install)
- Easy to setup a single context(pass the state value to context and then provide it to the app)
- additional state 'slide' requires new context setup from scratch(provider hell in app.js)(create nother provider and custom hook)
- no mechanism for async function
- no performance optimization
- only react dev tools

# Redux

- requires additional package(large bundle size)
- more work to setup initially
- once set up its easy to create additional state slices(all you need to do it create another slice and the reducer)
- support for async functions by providing middleware
- performance is optimized out of the box.
- excellent dev tools

# Usage of ContexAPI + useReducer:

- use this for global state management in small apps
- when you just need to share a value that does not change very often(color theme,preferred language,authenticated user)
- when you need to solve the simple prop drilling problems.
- when you need to manage statein a local sub-tree of app

# Usage of Redux:

- use this for global state in small apps
- when you have lots of global UI states that needs to be updated frequently(because redux is optimized for this)(shopping carts,current open tabs,complex filters or search)

- when you have complex state with nested objects and arrays because you can mutate state with redux toolkit
