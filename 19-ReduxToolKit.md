# Redux Tool Kit

- built on top of classic Redux
- modern and preferred way of writing redux code
- opinionated approach forcing us to use the redux best practises
- 100% compatible with classic redux , allowing us to use them together.
- You can use classic redux in one part of the app and the modern redux tookit in other part

# Actual Advantages of Redux ToolKit.

- allow us to write a lot less code to acheive the same result.
- redux toolkit set up thing by itself like (setting up middleware and redux developer tools).

# Redux Toolkit gives are 3 big things out of the box:

- allows us to write code that "mutates" state inside reducers (will be converted to immutable logic behind the scenes by "Immer" library).New code that we will write will look as if we are mutating the state directly.This is the biggest advantage of using redux toolkit because if uou have pretty complex state object with nested objects and arrays this can be a game changer in reducing complexity.
- this automatically creates action creators from our reducers
- automatically setup thunk middleware and DevTools.

# createSlice in Redux Toolkit:

- redux toolkit gives us the createSlice method which will do three things automatically for us:
- 1-automatically create action creators for us from the reducer
- 2-it makes writing reducers a lot easier for us.(we do not need switch statements and the default case is also automatically handled for us)
- 3- we can actually mutate our state inside reducers(Behind the scenes: Immer will convert our logic back into immutable logic)
