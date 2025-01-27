# Extend the Functionality of Reduc Using Middleware

- where we can make API calls (asynchronous data fetching) in redux?
- we can not make API calls inside reducer because reducers need to be pure functions with no side effects.
- It only knows how to synchronously dispatch actions.
- Asynchronous operations like API calls need to happen outside of reducer.
- maybe we should fetch data inside a components then dispatch the action to the store with data received data.This is actually possible but not ideal soultion as we want to keep our components clean and free of data fetching.
- So it can not be inside redux store and also not in components.

# So where do we keep our data fetching logic.

## Solution : MIDDLEWARE

- Middleware is a function that sits between dispatching the action and the store.Allows us to run code after dispatching action and before that action reaching the reducer in the store.
- Usually after we dispatch the action,immediately reaches the reducer and state is updated.But with the middleware we can do something with the action before that action gets into reducer in store.
- So this is perfect place for asynchronous data fetching.
- So middle ware is perfect place for side effects.
- In case of asynchronous operations most popular middleware is reduc thunks

# How Thunks Middleware works?

The action will no longer be immediately dispatched but first go into middleware.

```code
{type:'deposit'
payload:50
}
```

- The we can start fetching data inside middleware(for example take deposit money in any currency then convert the value of deposit to USD using an external currency converter)

```code
{type:'deposit'
payload:{data}
}
```

- basically thunks allows redux to wait for fetching data

## How to use Middleware

- install middleware package.
- then we apply that middleware package to our store.
- then we use middleware in our action creator functions.

## Conclusion:

- In react when we are using Thunks insted of returning an action object from the action creeator function we return a new function. And result of deposit({type:'account/deposit',payload:amount}) becomes a function.So redux when sees that we are dipatching a function into which we are passing a dispatch function and getState.Then we can use that dispatch function to delay dispatching until async operation we want to implement finishes.So therefore we can think of the thunks function sitting between initial disatching and the reducer of the store receiving action.
