# useNavigate : Programmatic Navigation (moving to a new URL withour the user having to click on any link)

use case : redirecting to anew page right after submitting a form

# create a route :

```code
<route path="form" element={</Form>}/>
```

# redirecting to that route path

now in our map component we want that whenever user clicks on something the route get redirected to a new route localhost:3000/form

first call useNavigate hook

```code
const navigate = useNavigate();
```

then call this navigate method whereever you want to redirect it

```code
//imperative way of routing
<div onClick={()=>navigate('form')}></div>
 onClick={()=>navigate(-1)}
```

# Navigate Back:

onClick={()=>navigate('form')}
