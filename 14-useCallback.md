# useCallback

```code
const handleAddPost = useCallback(function handleAddpost(post){
setPosts((posts)=>[...posts,post])
})
```

useCallback will simply store the function which will be called later in code
state setter functions of useState are automatically memoized
