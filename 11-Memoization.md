# Memoization

Optimization technique that executes a pure function once and saves the result in memory.If we try to execute the function once again with the same arguments as before previously saved results will be returnd without executing the function again.

function A --> Call function A --> store results in cache --> call Function A again with same inputs --> cached results will be returned ---> if called with different inputs --> new results will be calculated

## Tools for Memoization

- memoize components with memo function
- memoize objects with useMemo
- memoize functiond with useCallback

## Benefits of memoization

This will improve app speed and responsiveness by preventing wasted renders

## memo Function--memoized components

- used to create a component that will not re-render when its parent re-render as long as the props stay same between the renders.
- in regular behavious of react when parent re-render the child will re-render even if props passed to child remian the same.
- memoization only affects the props -- a memoized component will still re-render when its own state changes or when a context that it is subscribed to changes.
- memoization only makes sense when a components is heavy,re-renders often , and does so with the same props

## How to use memo for the memoization of the components:

simply wrap entire component inside memo() function call which will return a brand new components
const Archive= memo(function Archive(){}).

## Drawbacks of memo function

In react whenever a components instance is re-rendered everything in there is re-created and that includes objects and functions that are defined within components.New render gets new objects and functions even if they are same.
In JS two objects or functions that look exactly the same are actually two different ones.For example two emty objects are not same . ({} != {})
If Objects or functions are passed as props to child component.child component will always seee them as new props on each render.And if props are different between render our memo function simply does not work

## Summary:

If we memoize a component but then give it objects or functions as props then
the component will re-render anyway because it will always see props as new props even if they are same

## Solution:

So we need to make our objects and functions stable by preserving them between renders by memoizing them as well (useMemo--> memoize any value between render,useCallback-->memoize function)
