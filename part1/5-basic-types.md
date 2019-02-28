# Basic Types

## From the tour

- Basic Types:
  + bool
  + string
  + int, int8, int16, int32, int64, uint, uint8, uint16, uint32, uint64, uintptr (number types)
  + byte (alias for uint8)(number type)
  + rune (alias for int32)(number type)
  + int (number type)
  + float32, float64 (number types)
  + complex64, complex128 (number types)
- *"When you need an integer value you should use `int` unless you have a specific reason to use a sized or unsigned integer type"* This is because 'int' can hold any size of number, up to 64-bit
- *"Variables declared without an explicit initial value are given their zero value"*
- Zero Values:
  + 0 for numeric types
  + 'false' for booleans
  + "" (empty string) for strings

### Examples

##### Instantiating basic types
```
var b bool = true
var i int = 8
var s string = "Hey"
var f float64 = 3.1415
```

##### Instantiating those same basic types with shortcut
```
b := true
i := 8
s := "Hey"
f := 3.1415
```

##### Instantiating basic types without values
```
var b bool
var i int
var s string
var f float64
```
** Note that you can't use the shortcut to instantiate types with zero values, because there are no values for the shortcut to infer Type from
