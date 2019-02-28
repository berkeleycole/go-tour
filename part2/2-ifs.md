# If Statements

## From the tour
- *"...like in for loops; the expression need not be surrounded by parentheses but the braces are required"*
- *"Like 'for', the if statement can start with a short statement to execute before the condition"*
- *"variables declared in this statement are only in scope until the end of the if"*
- else blocks are declared as expected
- *"variables declared inside an 'if' short statement are also available in the if block"*
- the above otherwise states that a scope belongs to the entire 'if' block, not the 'if' and 'else' statements separately.

### Examples

##### Most Basic If Statement
```
if 3 < 4 {
  fmt.Println("TRUE")
}
```

##### If statements in functions
```
func isAdult(age int) bool {
  if age < 18 {
    return true
  }
  return false
}
```

##### If statements with variable
```
func scoreTotals(score1, score2, score3 int) (int, bool) {
  record := 42
  if total := score1 + score2 + score3; total > record {
    return total, true
  }
  return score1 + score2 + score3, false
}
```
A few things to remember from this:
- to return multiple values, they must be in parentheses ... I had forgotten
- notice that on line 34, I cannot 'return total, false' because total no longer exists. This would actually be a reason to create a local variable for the 'total' value ... Or use the else...

##### If with Else
```
func scoreTotals(score1, score2, score3 int) (int, bool) {
  record := 42
  if total := score1 + score2 + score3; total > record {
    return total, true
  } else {
    return total, false
  }
}
```
You can see here that though the implicit else is very helpful, using an else and the benefits of a scope shared with the 'if' statement dried up my code a bit.
