## useCallback is a special case of useMemo

whatever value is passed into useMemo() or useCallback() will basically be cached and stored in memory and cached value will be returned in future renders as long as inputs stay the same

- in case of useMemo & useCallback the input mentioned are called as dependencies.Just like useEffect hook useMemo & useCallback has dependecy array.
- Whenevr one of the dependencies change,the value will no longer be returned from the cache but instead will be recreated when props change.

## Why Memoization:

- memoizing props in order to prevent wasted renders(together with memo function )
- Memoizing values to avoid expensive re-calculations on every render.
- Memoizing values that are used in dependency array of another hook
