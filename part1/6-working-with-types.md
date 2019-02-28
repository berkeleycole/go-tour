# Working with Types

## From the tour
- Types are never 'accidentally' changed in Go.
- *"Unlike in C, in Go assignment between items of different types requires an explicit conversion."*
- Type conversion can be achieved by stating:
```
  desiredType(value or variable name)
```

### Examples

##### Type Conversions
```
var i int = 42
var f float64 = float64(i)
var u uint = uint(f)
```

##### Further
```
var i int = 42
var f float64 = float64(i)
var u uint = uint(f)
var s string = string(u)
```
** Some notes on this. The last conversion to string results in not `"42"` as I expected, but rather `*`. There are some reasons for this. And this is where the terms 'type casting' and 'type conversion' start to show their shades of difference. When I convert the int 42 to to a string, I turn the value of 42 into its string form (`"42"`). But that is not what I have done here: I have 'casted' the int 42's byte representation into a string, and in string land (or unicode) 42 bytes is an asterisk. Really, I have converted int 42 into bytes and then converted those bytes to a string.

** And more notes, there is a Go package for a true string conversion that would return `"42"`

** Outstanding question surrounding this code that returns an error:
```
var i int = 42
var u uint = uint(i)
var s string = string(u)
var u2 uint = uint(s)
```
why can I convert 'u' to a string on line 3, but can't reverse the process on line 4?
