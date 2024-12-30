# State Management Tools & Type of States

## 1-Types on the base of State Accessibility

### local state

- needed only by one or few components
- only accessible in component and child components.

### Global state

- Needed by many components
- accessible to every component in the application

# How to identify the state as global or local state

Notice that if a component is rendered twice then the state update in one of the component should be reflected inside the other components . If answer is yes then you should use global state otherwise use local one

## 2- Types on the basis of State domain

### Remote state

- All application data is loaded from the remote server(API).A state that lives on server but is loaded using an API into our application
- loaded in a asynchronous manner
- needs to be refetched and updated

### UI State

- everything else
- selected theme,form inputs,applied list filters,open panels
- synchrously fetched and stored right in the application

# Where to Place the State:

## local state :

- can be placed in a local components
- tools : useState, useReducer , useRef(refs does not re-render the component)

- sometimes a state is needed by many components , so we lift the state up and place it in the parent component of all the child components ,
- placed in parent component
- tools : useState, useReducer , useRef

## Global state(ui state) :

- placed in context
- preferable when global state(ui state)
- tools : Context Api , useState , useReducer
  keep in mind that context does not manages the state we still need useState and useReducer to manage the state , but context is used to provide that state to alk the components which need that piece of state

## Global State (especially remote state , generally both remote and Ui )

- tools :Redux,React Query,SWR, Zustand

## URL state(excellent place for storing global state that we want to make accessible to all all the components )

- tools : React router
- when to use : when state is global and passing between components

## storing date in browser

- tools : local storage, session storage,

# State Management Tools Options

how to manage different types of state in practise

- Local UI state
- Global UI state
- Remote Local state
- Remote Global state

## Local UI state:

- useState
- useReducer
- useRef

## Remote Local state: (in small application)

- fetch + useEffect + useState/useReducer

## Remote Global State: (in bigger applications we treat all the remote state as global state)

- tools highly speciallized in managing remote state:(react query,SWR ,RKT query) these tools have built in mechanism for caching and refetching
- redux, zustand, recoil
- contextAPi, useState,useReducer

## Global UI State:

- contextApi+useState/useReducer
- react router
- redux, zustand, recoil
