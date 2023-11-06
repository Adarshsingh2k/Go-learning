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

