# Loops

## From the tour
- *"Go has only one looping construct, the 'for' loop"*
- *"The basic 'for' loop has three components, separated by semicolons: the init statement...the condition expression...the post statement"*
- *"The init and post statements are optional"*
- If you drop the init and post statements, you don't need the semicolons
- To create an infinite loop, just leave off the condition statement as well
* I don't know why they say that the init and post statements are optional and then say you can drop the conditional if you want an infinite loop....might as well just say that all statements are optional, you just don't typically want an infinite loop.

### Examples

##### Basic 'for' Loop
```
func main() {
  for i := 0; i <= 10; i++ {
    fmt.Println(i)
  }
}
```
Of course, the code above has absolutely no purpose to the rest of the program yet...

##### More Useful 'for' Loop
```
  func main() {
    sum := 0
    for i := 0; i < 10; i++ {
      sum += i*i
    }
  }
```
Here we are adding to 'sum' after each iteration...slightly more useful

##### Optional statements
```
func main() {
  total := 0
  for ; total < 20; {
    total += 1
  }
}
```
.... or .... without the extra semicolons:
```
func main() {
  total := 0
  for total < 20 {
    total += 1
  }
}
```
Again a simple example, but shows that when the variable created for the loop is just extra, you don't have to use it.

##### But what about this...
```
func main() {
  total := 0
  for total < 10; total++ {
    ...nothing
  }
}
```
Don't know if this is allowed or how to handle this really, might be better to write as above in 'Optional Statements', moving the post statement down into the body.

##### The Forever Loop
```
func main() {
  for {
    fmt.Println("...This is the song that never ends...")
  }
}
```
