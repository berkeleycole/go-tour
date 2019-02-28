# Functions

## From the tour
- *"Notice that the type comes after the variable name."*
- After arguments, give the type that should be returned

### Examples

##### Basic adding function:

```
func add(x int, y int) int {
  return x + y
}
```

##### Basic adding function with argument shortcut:

- *"When two or more consecutive named function parameters share a type, you can omit the type from all but the last."*

```
func add(x, y int) int {
  return x + y
}
```

##### Function returns:

- *"A function can return any number of results"*
- this is cool! Its a weird thing for me to get used to, but its cool

```
func swap(x, y string) (string, string) {
  return y, x
}
```

##### Named returns:

- *"Go's return values may be named. If so, they are treated as variables defined at the top of the function"*
- *"These names should be used to document the meaning of the return values"*
- *"A return statement without arguments should be used only in short functions. This is known as a `naked` return."*
- Below is an example of a naked return ... *"Naked return statements should only be used in short functions, as they can harm readability in longer functions"*

A short naked function
```
func split(sum int) (x, y int) {
    x = sum * 4 /8
    y = sum - x
    return
}
```

- Below is an example of a normal named return function
```
func concat(x, y string) (concated string) {
  concated = x + " " + y
  return concated
}
```
