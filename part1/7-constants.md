# Constants

## From the tour
- *"Constants are declared like variables, but with the 'const' keyword"*
- *"Constants can be character, string, boolean, or numeric values"*
- *"Constants cannot be declared using the := syntax"*
- The values contained within constants cannot be changed
- An untyped constant infers type from its context, just like variables
- *"Numeric Constants are high precision values"*

### Examples

##### Declaring Constants
```
const Age int64 = 64
```

##### Rules of Constants
The code below creates an error 'cannot assign to Age'
```
const Age int64 = 64
Age = 13
```

##### Big Numbers
...not sure I understand this entirely...will come back to it.
