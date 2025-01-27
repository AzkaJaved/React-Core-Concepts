in cases where you have one slow component inside another component which update
the slow component then you can use this optimization technique.

```code
function Parent(){
    return(
        <button onclick={()=>count+1}>Increase count :{count}</button>
        <SlowComponent>
    )
}
```

we pass SlowComponent into the counter as children.

```code

function Counter({children}){
    return(
        <button onclick={()=>count+1}>Increase count :{count}</button>
        {children}
    )
}
function Parent(){
    return(
        <Counter><SlowComponent/></Counter>
    )
}
```

SlowComponent has this time been passed as children prop.This means that SlowComponent was already created before the counter component re-rendered.So there is no way this components has been affected by the state change in parent.
React will look at JSX above and it will create SlowComponent and Pass it into the Counter Component all while rendering.When we increase the count the Counter component is re-rendered.But SlowComponent has already been rendered and passed as a prop.So it can not be affected by the state change

Whenever the parent component re-renders, all of its children that receive props from it are re-rendered
Any child that receives new or changed props will re-render.

- If a child component’s props haven’t changed, React will not re-render it unless:
- The child is explicitly forced to update.
- The child is not memoized.
