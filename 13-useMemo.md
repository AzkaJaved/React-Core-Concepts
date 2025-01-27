# useMemo

- useMemo takes in a callback function

```code
const archiveOptions = useMemo(()=>{
return {
show:false,
title:'Show Archive'
}
},[])
```

- useMemo() will memoize the result of simply calling this callbackFunction which is present in it.useMemo stores the result of the function call which is simple the value.
- empty depdency array means that this value will only be calculated once in begining.
  If you do not provide any variable inside dependency array then useMemo will never be called again and calculations will only be done in the begining after that the useMemo will remember old data from the cache this is called as Stale Closure(values refrenced to are the values which were at the time when function was created)
