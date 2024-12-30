# useParams : Extracts Dynamic Routing Segments from URL's Path

Allows components to react dynamically to URL changes.
Facilitates routing for pages that depend on identifiers like user IDs or product IDs.

to use params with react router,we do it in three steps

## 1- create a route

:nameOfParams

```code
<route path='citites/:id' element={<City/>} />
//whenever the URL takes this shape like localhost:3000/cities/:id then react will render the City componenet on screen
```

## 2-link the route

if we add / befor id like /${id} then it will go to root url first and then add the id of the city.But we want to attch the id of the city to the end off the current URL so we will not add this /.

```code
<Link to={`${id}`}>city</Link>
```

## 3- Read the state from the route

To get that data fromt he URl we will use useParams() hook.

```code
const id = useParams()
```

# Use useParams for routing and identifying resources by IDs or other dynamic path segments.

# Use useSearchParams for features like search, filtering, or maintaining temporary UI state in the URL.
