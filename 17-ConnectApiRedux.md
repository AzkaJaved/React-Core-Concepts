# Connect API IN Redux (old way of connecting react app to Redux before useSelector and useDispatch)

- besides exporting useSelector and useDispatch React Redux also exports Connect API.
- the connect function takes in another function which in turn will return another funtion which will accept our component as new argument.The function is called mapStateToProps().
- This function will receive the state props which will return object containing the name of prop which will be recived by our component.

```code
function mapStateToProps(state){
    return {
       balance:state.account.balance
    }
}
```

```code
export default connect(mapStateToProps)(BalanceDisplays);
```

- connect(mapStateToProps) becomes a function
- BalanceDisplay function then becomes the argument to the new function connect(mapStateToProps).
- The BalanceDisplay will then receive the new prop.
- Now you can use the new balance prop in your component BalanceDisplay
