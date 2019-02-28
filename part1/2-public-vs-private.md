# Private or Public

## From the tour:

- *"In Go, a name is exported if it begins with a capital letter."*
- *"When importing a package, you can refer only to its exported names."*

### Examples

##### Doesn't work
```
fmt.Println(math.pi)
```
RETURNS ERROR: can't load package: package main:
prog.go:1:1: illegal character U+0023 '#'

##### Does work
```
fmt.Println(math.Pi)
```
RETURNS `3.141592653589793`
