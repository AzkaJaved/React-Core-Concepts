# Performance Optimization in React Apps

there are three areas we can work on when it come to performance optimization in react apps

## try to Prevent wasted Renders

- memoize components with memo
- memoize functions and objects with useMemo and useCallback hooks
- pass elements into other elements as children or as normal prop

## Improve app speed and responsiveness

- useMemo
- useCallback
- useTransition

## Reduce bundle size

- use 3rd party packages
- code splitting and lazy loading

## When exactly a component instance gets re-rendered

- whenever state changes
- whenever there is a change in context that the component is subscribes to
- whenever a parent component re-renders all of its child components who receive props from it will re-render anyway.
- rendering a component does not mean that the DOM actually gets updated,it just means the component function gets called.But this can be expensive & wastefull operation.A wasted render is a render that does not produce any change in the DOM

## Profiler

components with gray color are acutually the components that did not render
more yellow the color more time it took to render
