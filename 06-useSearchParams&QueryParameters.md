# useSearchParams : hook for accessing query parameters

Manages query parameters in the URL (example: ?search=React&category=hooks).
Helps read and manipulate query strings.

# Setting the Query Parameters

```code
<Link to={`${id}?lat=${position.lat}&lng=${position.lng}`}></Link>
```

# Getting the value for query parameters.

```code
 const [searchParams, setSearchParams] = useSearchParams();

  const lat = searchParams.get('lat'); // Get the value of 'lat'
  const lng = searchParams.get('lng'); // Get the value of 'lng'
```

# Use useParams for routing and identifying resources by IDs or other dynamic path segments.

# Use useSearchParams for features like search, filtering, or maintaining temporary UI state in the URL.
