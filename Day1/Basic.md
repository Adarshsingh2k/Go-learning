## Basics Of Go

### Basic Datatyps ( Primitive )

bool

string

int int8 int16 int32 int64
uint uint8 uint16 uint32 uint64 uintptr

byte // alias for uint8

rune // alias for int32
// represents a Unicode code point

float32 float64

complex64 complex128

Sure, if you'd like to convert the explanation about variables in Go into a Markdown format, it might look something like this in a `README.md` file:

# Variables in Go

In Go, variables are storage identifiers that hold data. Each variable has a specific type, which dictates what kind of data it can hold. Below are various ways to declare and initialize variables in Go.

## Declaring Variables

- **Using the `var` Keyword**: Declare a variable with `var`, followed by the name and type.

  ```go
  var x int
  var name string
  var isAvailable bool
  ```

- **Declaring Multiple Variables**: Declare multiple variables of the same type in one statement.

  ```go
  var x, y, z int
  ```

- **Initializing Variables**: Initialize variables with values upon declaration.

  ```go
  var x int = 5
  var name string = "Alice"
  var isAvailable bool = true
  ```

- **Type Inference**: Skip the type on initialization, and Go will infer it.

  ```go
  var x = 5 // int
  var name = "Alice" // string
  var isAvailable = true // bool
  ```

- **Short Variable Declaration**: Use `:=` inside functions to declare and initialize.
  ```go
  x := 5
  name := "Alice"
  isAvailable := true
  ```
  > Note: The `:=` syntax can only be used within functions.

## Package-Level Variables

Variables declared at the package level are accessible anywhere within the same package.

```go
var (
    ExportedVar   = "Accessible from other packages."
    privateVar    = "Only accessible within my own package."
)
```

## Pointers, Arrays, and Other Types

Variables in Go can be of various types, such as pointers, arrays, slices, and more.

```go
var pointer *int
var numbers [5]int
var slice []int
var lookup map[string]int
var channel chan int
var function func(string) int
```

## Zero Values

Variables declared without initialization are set to their type's zero value.

- Numeric types: `0`
- Boolean type: `false`
- String type: `""` (empty string)
- Nil for pointers, functions, interfaces, slices, channels, and maps

# For Loops in Go

The Go programming language provides a single `for` loop construct that can be used in various ways to iterate over data structures or to create loops of different kinds. This document outlines the different usages of `for` loops in Go.

## Simple Loop

A loop that continues until a condition is no longer true.

```go
for condition {
    // code to execute
}
```

Example:

```go
i := 0
for i < 10 {
    fmt.Println(i)
    i++
}
```

## Classic For Loop

The traditional `for` loop with an initializer, condition, and post statement.

```go
for initializer; condition; post {
    // code to execute
}
```

Example:

```go
for i := 0; i < 10; i++ {
    fmt.Println(i)
}
```

## For-Range Loop

Iterate over elements of arrays, slices, strings, maps, and channels.

```go
for key, value := range collection {
    // code to execute
}
```

Example for a slice:

```go
slice := []int{1, 2, 3, 4, 5}
for i, value := range slice {
    fmt.Println(i, value)
}
```

Example for a map:

```go
m := map[string]string{"a": "Apple", "b": "Banana"}
for key, value := range m {
    fmt.Println(key, value)
}
```

## Infinite Loop

Loops indefinitely until `break` is called or an enclosing function returns.

```go
for {
    // code to execute
}
```

Example:

```go
for {
    fmt.Println("Looping indefinitely")
    break // will exit the loop
}
```

## Loop with Continue

Skip the rest of the current loop iteration and continue with the next.

```go
for i := 0; i < 10; i++ {
    if i%2 == 0 {
        continue
    }
    fmt.Println(i) // will print odd numbers
}
```

## Loop with Break

Exit the loop before it completes all its iterations.

```go
for i := 0; i < 10; i++ {
    if i > 5 {
        break
    }
    fmt.Println(i)
}
```

## Conclusion

The `for` loop is a powerful control structure in Go that can handle a variety of iterative tasks with simplicity and clarity. Use the examples above as a starting point for implementing your own `for` loop logic in Go programs.


