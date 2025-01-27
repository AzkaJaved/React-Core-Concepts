## @layer base{}

@ layer base{

}
base layer in tailwind css targets all the html elements.

## @layer utilities{}

@layer utilities {

}
we can add any utility classes which will modify one or two styles for particular class name

## @layer components{}

if we wanted to create a .btn className for a button

## How to use @layer directives

we can use apply directive which will apply all the styles asociated with particular class of tailwind

```code
@ layer base {
    h1,h2,h3,h4,h5,h6{
       @apply font-bold
    }
}
```
