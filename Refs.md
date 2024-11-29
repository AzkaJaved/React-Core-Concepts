# useRef

Any data that you want to preserve/persist between renders is stored in refs.Their current property value remians same accross multiple renders
When we use useRef , react will give us an object with mutable current property.We can then write any data into this mutable current property and of course read from it

# use cases for refs

1 - Creating a variable that stays the same accross multiple renders like (storing previous state and storing the id of setTimeOut function)
2 - Selceting and storing DOM elements.
Refs are fro data that is not rendered on screen(in the visual outputs) usuallyonly appear inevent handlers or effects . Not in JSX(for elements/data that appears in useState we use useState )
Do not read or write current property in render logic(like useState).We usually perform these mutations inside useEffect hook

# Similarities & Differences between useRef and useState.

1- Similarity: Both useState and useRef persist data across re-renders.
2- Difference: Updating state causes the component to re-render but updating refs does not cause the component to re-render.
3- Diference : State is immutable but refs are mutable
4- Diference : State is updated asynchronously it means we can not use new state immediately after updating it.With refs updates are not asynchronous.So we can basically read new current property immediately after updating it.basically just like any other regular JS object

# Takeaway :

we use state when we want to store data that shoul re-render the component and refs for data the should only be remembered by the component overtime but never re-render it.
