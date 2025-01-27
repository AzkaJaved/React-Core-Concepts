- Redux is a third-party library for managing global state in a web-application
- Standalone library,we can use it with any frmawork of even vanilla JS, But it is very easy to integrate react apps using react-redux library
- All global state is stored in one globally accesible store,which is easy to update using actions (like useReducer)
- when global store is updated all the consumers of the state will also update

## Two versions of Redux:

- Classic redux
- Modern Redux toolkit

## What is Redux:

- All global state is stored in one globally accessible store which is easy to update using actions (like useReducer).
- when global store is updated ---> all consuming components re-render.
- it is conceptually similar to using contextAPI + useReducer.
- two versions of react .

1. classic Redux.
2. Redux toolkit.

## Many apps do not need redux anymore,unless they need a lot of global UI state.

### UI State.

- state that is not fetched from server
- data about ui or data does not need to be communicated to an api or so.

### Remote State.

- for global remote state we have now more specialized tools like SWR,Redux toolkit.

### How Reducer Works.

- when we want to update state form an event handler in a component we start by creating action.This action is an object that contains information about how the reducer should update state.(type and payload)
- then we dispatch that action to a reducer function.
- the reducer takes the action type and payload together with the current state calculates new state.
- state updates and component which orignates state transition re-renders

### How Redux works different from useReducer.

- in redux we simply dispatch actions not to reducer function but to a store.
- All global state lives in this centralized container.It is single source of truth of global state in the app.
- store can have multiple reducers.
- Each reducer is pure function that calculates new state based on action and current state.Usually one reducer per app feature (one reducer for theme,one for user data,one for shopping cart)
- In Redux we Usually use functions called ACTION CREATORS in order o automate the process of writing actions.

## Redux Cycle:

- In order to update global state using redux we start by calling action creators in a component and dispatch the action that resulted from the actio creator.This action will reach store where the right reduer will pick ut up and update the state according to the instructions.

## Goal of Redux:

Makes the state update logic separate from the rest of the application

## Action Creators

- action creators are nothing but functions that return actions.
- action creators are not a redux thing but they are additionally created functions for ease and redux would work fine without them
