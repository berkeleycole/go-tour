# Variables

## From the tour
- *"The var statement declares a list of variables"*
- *"The type is last"*
- *"A var statement can be at package or function level"*
- There seems to be no difference between vars declared at function or package level, what is important is where they are declared

### Examples

##### Var declarations

Both package and function level variable declarations
```
var a, b, c string

func main() {
  var i int
  var b bool
}
```

##### Var declarations with initial values

- *"A var declaration can include initializers"*
- *"If an initializer is present, the type can be omitted; the variable will take the type of the initializer"*
- Example of multiple variable declaration with type:
```
var i, j int = 1, 2
```
- Example of multiple variable declaration without type:
```
var a, b, c = true, false, "no!"
```

##### Short variable declarations

- *"The := short assignment statement can be used in place of a `var` declaration with implicit type"*
- *"Outside a function, every statement begins with a keyword (`var`, `func`, etc...)" - so short assignment won't work.*
Example with var keyword and stated type
```
  var i, j int = 1, 2
```

Example with var keyword and implicit type
```
  var i, j = 1, 2
```

Example with short assignment construction
```
func main() {
  i, j := 1, 2
}
```
