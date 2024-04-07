###This is my 1st fundamental level Golang project. 

```go
package main
import (
    "fmt"
)

func main() {

    fmt.Println("Welcome to my Simple Calculator") // Moved inside the main function.

    var num1, num2, result float64
    var operations string

    fmt.Print("Enter the 1st number: ")
    fmt.Scanln(&num1) // Consider handling the error returned by Scanln.

    fmt.Print("Enter the 2nd number: ")
    fmt.Scanln(&num2) // Consider handling the error returned by Scanln.

    fmt.Print("Choose the Operator which you want (+,-,/,*): ")
    fmt.Scanln(&operations)

    switch operations {
    case "+":
        result = num1 + num2
        
    case "-":
        result = num1 - num2

    case "/":
        if num2 == 0 {

            fmt.Println("Cannot Divide by zero, Try Again!!!")
            return

        }
        result = num1 / num2

    case "*":
        result = num1 * num2

    default:
        fmt.Println("You entered the wrong operator, Please use only these operators (+,-,*,/)")

        return
    }

    fmt.Printf("Result: %f\n", result)

}
```
