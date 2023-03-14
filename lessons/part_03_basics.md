# Go lessons

> Go is a statically-typed programming language designed for building efficient, reliable, and scalable software

## Go Basic Syntax Training

Hey there, let's dive into the basic syntax of Go! In this article, we'll cover all the basic elements of the language,
such as keywords, identifiers, literals, operators, variables, standard data types, constants, language syntax,
comments, and statements. We'll use informal language and plenty of examples to make learning fun and engaging.

### Keywords

Go has a total of 25 keywords, which are reserved for use by the language itself. Here's a list of all the keywords:

| keyword  | -           | -           | -           | -      |
|----------|-------------|-------------|-------------|--------|
| break    | default     | func        | interface   | select |
| case     | defer       | go          | go          | go     |
| chan     | else        | goto        | package     | switch |
| const    | fallthrough | fallthrough | fallthrough | type   |
| continue | for         | import      | return      | var    |

These keywords cannot be used as identifiers, such as variable or function names, and should be used only for their
intended purpose.

Let's take a closer look at each of these keywords and their usage.

- `break`: Used to terminate a loop or switch statement.
- `case`: Used within a switch statement to define different cases.
- `chan`: Used to define a communication channel for goroutines.
- `const`: Used to declare a constant value.
- `continue`: Used to skip the current iteration of a loop and move to the next one.
- `default`: Used within a switch statement to define the default case.
- `defer`: Used to schedule a function call to be executed after the current function completes.
- `else`: Used within an if statement to define the alternative path.
- `fallthrough`: Used within a switch statement to move to the next case, even if it doesn't meet the condition.
- `for`: Used to define a loop.
- `func`: Used to define a function.
- `go`: Used to start a new goroutine.
- `goto`: Used to jump to a label in the current function.
- `if`: Used to define a conditional statement.
- `import`: Used to import a package.
- `interface`: Used to define an interface.
- `map`: Used to define a map data structure.
- `package`: Used to define a package.
- `range`: Used to iterate over a collection, such as an array, slice, or map.
- `return`: Used to return a value from a function.
- `select`: Used to wait on multiple communication operations.
- `struct`: Used to define a struct data type.
- `switch`: Used to define a switch statement.
- `type`: Used to define a new type.
- `var`: Used to declare a variable.

> It's important to remember that keywords cannot be used as names for variables, functions, or other identifiers in
> your program

### Identifiers

Identifiers in Go are used to identify the names of variables, functions, constants, and types. An identifier is a
sequence of letters, digits, and underscores (_) that begins with a letter or an underscore. Identifiers are
case-sensitive in Go, which means that the names "hello" and "Hello" are considered different.

Examples of valid identifiers in Go:

```text
age
userName
user_name
User_Name
a1
```

Examples of invalid identifiers in Go:

```text
1user (cannot begin with a digit)
my-user (cannot include a hyphen)
my user (cannot include whitespace)
```

It is important to use descriptive and meaningful identifiers to make your code more readable and understandable.

### Literals

In programming, literals refer to fixed values that are hardcoded into a program's source code. In Go, there are several
types of literals:

1. Integer literals: These are whole numbers and can be represented in decimal, binary, octal, or hexadecimal formats.

   Examples:
   ```text
   42       // decimal
   0b101010 // binary
   0o52     // octal
   0x2a     // hexadecimal
   ```
2. Floating-point literals: These are numbers with decimal points or exponents.

   Examples:
   ```text
   3.14      // floating-point
   6.022e23 // scientific notation
   ```
3. Rune literals: These are single Unicode characters and are represented in single quotes.

   Examples:
   ```text
   'a'
   '好'
   '\n'
   '\t'
   ```
4. String literals: These are sequences of characters and are represented in double quotes.
   Examples:
   ```text
   "Hello, world!"
   "你好，世界！"
   "I am a string with a\nnew line!"
   ```
5. Boolean literals: These are either `true` or `false`.

### Operators

Operators are used to perform operations on operands (variables, constants, and expressions) in a program. Go supports
various types of operators, including arithmetic operators, comparison operators, logical operators, and bitwise
operators.

Here's a brief overview of the different types of operators in Go:

**Arithmetic Operators**:
Go supports all the basic arithmetic operators like addition `+`, subtraction `-`, multiplication `*`, division `/`, and
remainder `%`. For example:

```go
package main

import "fmt"

func main() {
	x := 10
	y := 5
	fmt.Println(x + y) // Output: 15
	fmt.Println(x - y) // Output: 5
	fmt.Println(x * y) // Output: 50
	fmt.Println(x / y) // Output: 2
	fmt.Println(x % y) // Output: 0
}
```

**Comparison Operators:**
Go also supports comparison operators to compare two values. These include `==` (equal to), `!=` (not equal to), `<` (
less than), `<=` (less than or equal to), `>` (greater than), and `>=` (greater than or equal to). For example:

```go
package main

import "fmt"

func main() {
	x := 10
	y := 5
	fmt.Println(x == y) // Output: false
	fmt.Println(x != y) // Output: true
	fmt.Println(x < y)  // Output: false
	fmt.Println(x <= y) // Output: false
	fmt.Println(x > y)  // Output: true
	fmt.Println(x >= y) // Output: true
}
```

**Logical Operators:**
Go supports logical operators to perform logical operations on boolean expressions. These include `&&` (logical
AND), `||` (logical OR), and `!` (logical NOT). For example:

```go
package main

import "fmt"

func main() {
	x := true
	y := false
	fmt.Println(x && y) // Output: false
	fmt.Println(x || y) // Output: true
	fmt.Println(!x)     // Output: false
}
```

**Bitwise Operators:**
Go also supports bitwise operators to perform operations on binary numbers. These include `&` (bitwise AND), `|` (
bitwise OR), `^` (bitwise XOR), `<<` (left shift), and `>>` (right shift). For example:

```go
package main

import "fmt"

func main() {
	x := 10             // Binary representation: 1010
	y := 5              // Binary representation: 0101
	fmt.Println(x & y)  // Output: 0
	fmt.Println(x | y)  // Output: 15
	fmt.Println(x ^ y)  // Output: 15
	fmt.Println(x << 1) // Output: 20 (Binary representation: 10100)
	fmt.Println(x >> 1) // Output: 5 (Binary representation: 101)
}
```

### Variables

In Go, variables are used to store values. They can be of different types, including the built-in types like int, float,
and bool, as well as custom types created by the programmer.

To declare a variable, you use the `var` keyword followed by the variable name and the type. Here is an example:

```text
var x int
```

This declares a variable named x of type int.

You can also initialize the variable with a value at the time of declaration like this:

```text
var x int = 10
```

This initializes the variable x with the value of 10.

You can also use the shorthand notation to declare and initialize a variable at the same time like this:

```text
x := 10
```

This declares a variable named x of type int and initializes it with the value of 10.

Go also supports multiple variable declarations in a single line:

```text
var x, y int
```

This declares two variables named x and y of type int.

You can also initialize multiple variables in a single line:

```text
var x, y int = 10, 20
```

This initializes two variables named x and y of type int with the values of 10 and 20, respectively.

As with other programming languages, you can also assign values to variables using the = operator:

```text
var x int = 10
...
x = 30
```

This assigns the value of 30 to the variable `x`.

Variables in Go can also be assigned the value of an expression, like this:

```text
z := x + y
```

This declares a variable named `z` and assigns it the value of the expression `x + y`.

One thing to note is that Go is a statically-typed language, which means that once you declare the type of a variable,
you cannot change it later on. For example, if you declare a variable of type `int`, you cannot assign a `string` value
to it later on.

Overall, variables are an important part of Go programming and are used extensively in the language.

### Data types

In Go, there are several basic data types that can be used to define variables. These data types include:

- `bool`: This data type represents a boolean value, which can be either true or false.
- `string`: This data type represents a string of characters, such as a word or a sentence.
- `int`: This data type represents an integer value, which can be either signed or unsigned.
- `float`: This data type represents a floating-point value, which can be either single-precision or double-precision.
- `complex`: This data type represents a complex number, which consists of a real and an imaginary part.
- `byte`: This data type represents a single byte of data.
- `rune`: This data type represents a Unicode character.

Here is an example of how to declare variables using these data types:

```go
package main

import "fmt"

func main() {
	var a bool = true        // type can be omitted here 
	var b string = "hello"   // type can be omitted here
	var c int = 10           // type can be omitted here
	var dx = 3.14            // omitting type in pre-initialized variable   
	var d float32 = 3.14     // type can not be omitted here
	var e complex64 = 1 + 2i // type can not be omitted here
	var f byte = 'a'         // type can be omitted here
	var g rune = '東'        // type can be omitted here

	fmt.Println(a)
	fmt.Println(b)
	fmt.Println(c)
	fmt.Println(d)
	fmt.Println(dx)
	fmt.Println(e)
	fmt.Println(f)
	fmt.Println(g)
}

```

In this example, we declare variables of each of the basic data types and assign them values. We then print out the
values of these variables using the fmt.Println function.

It's worth noting that Go also has several composite data types, such as arrays, slices, maps, and structs, which are
used to group together values of different data types.

#### Let's dive deeper into Go's built-in data types.

**Integers**: Go provides signed and unsigned integers of different sizes,
including `int8`, `int16`, `int32`, `int64`, `uint8`, `uint16`, `uint32`, and `uint64`. There is also a `uintptr` type,
which is an unsigned integer type that is large enough to store a pointer value.

**Floating-point numbers**: Go provides `float32` and `float64` data types for representing floating-point numbers.

**Complex numbers**: Go provides `complex64` and `complex128` data types for representing complex numbers. These types
consist of a real and imaginary component.

**Booleans**: Go provides a bool data type for representing Boolean values. The possible values are `true` and `false`.

**Strings**: Go provides a string data type for representing strings of characters. Strings are represented using double
quotes, e.g. "hello world".

**Arrays**: Go provides a fixed-size array data type, which is declared using brackets `[ ]` and the size of the array.
For example, `var arr [5]int` declares an array of integers with 5 elements.

**Slices**: Go provides a dynamic `array` data type called a `slice`, which is a reference to an underlying array.
Slices are declared using brackets `[ ]` without a size. For example, `var slice []int` declares a slice of integers.

**Maps**: Go provides a hash table data type called a `map`, which is a collection of key-value pairs.
Maps are declared using the `map` keyword, e.g. `var m map[string]int` declares a map with string keys and integer
values.

**Structs**: Go provides a struct data type, which is a collection of fields.
Structs are declared using the struct keyword,e.g. `type Person struct { name string; age int }` declares a Person
struct with name and age fields.

**Pointers**: Go provides a pointer data type, which holds the memory address of a variable. Pointers are declared using
the * operator, e.g. var ptr *int declares a pointer to an integer.

#### Type definitions and type aliases

It's important to note that Go also provides `type aliases`, which allow you to declare a `new type` that is simply an
alias for an existing type. For example, type `Celsius float64` declares a new type called `Celsius`.

Here's some information about the difference between `type definitions` and `type aliases` in Go:

In Go, you can create a new type by defining a new type with the `type` keyword.
This allows you to create a completely new type with its own underlying representation, even if it has the same
underlying type as an existing type.
For example, you could define a new type Miles that is based on the `float64` type:

```go
package sample

type Miles float64
```

With this type definition, you can create variables of type `Miles`:

```go
package sample

type Miles float64

var distance Miles = 10.5
```

You can also use this new type in function signatures:

```go
package sample

type Miles float64

func ConvertToKilometers(m Miles) float64 {
	return float64(m) * 1.60934
}
```

On the other hand, a type alias does not create a new type, but rather creates an alias for an existing type. This means
that the new type alias has the same underlying type as the original type, and can be used interchangeably with it. To
create a `type alias`, use the type keyword followed by the alias name and the original type:

```
type MyFloat float64
```

With this type alias, you can create variables of type MyFloat:

```
var x MyFloat = 3.14
```

Note that you can also create a type alias using the =, like so:

```
type MyFloat = float64
```

This syntax creates an alias for the `float64` type called `MyFloat`. However, using this syntax does not create a new
type; it simply creates an alias for an existing type.

In summary, the main difference between a `type definition` and a `type alias` is that a type definition creates a new
type with its own underlying representation, while a type alias creates an alias for an existing type. Depending on your
needs, you may choose to use one or the other.

### Constants

In Go, a constant is a variable whose value cannot be modified once it is assigned. Constants are used to define values
that remain the same throughout the program's execution.

To declare a constant in Go, we use the const keyword followed by the identifier and value. The syntax is as follows:

```
const identifier data_type = value
```

Here, identifier is the name of the constant, data_type is the data type of the constant, and value is the value
assigned to the constant.

For example:

```
const Pi float64 = 3.14159265359
```

In the above example, we have declared a constant named `Pi` of type `float64` with the value `3.14159265359`.

It is important to note that the value of a constant must be a constant expression, which means it must be able to be
evaluated at compile time.

Go also has some predeclared constants, such as `true`, `false`, and `nil`.
These are untyped constants, meaning they can be implicitly converted to any type.

For example:

```
const (
True  = true
False = !True
MaxInt = int(^uint(0) >> 1)
PiApprox = 22.0/7
)
```

Here, `True` and `False` are boolean constants, `MaxInt` is the maximum value for an int type, and `PiApprox` is an
approximation of Pi.

Constants can also be defined in terms of other constants, as long as the expression can be evaluated at compile time.

For example:

```
const (
a = 10
b = 20
c = a + b
)
```

Here, `c` is defined in terms of `a` and `b`.

In summary, constants in Go are variables whose values cannot be modified once they are assigned. They are declared
using the const keyword, followed by the identifier, data type, and value. Constant expressions must be able to be
evaluated at compile time.

### Language Syntax

Let's continue with a brief overview of the Go syntax.

Go has a syntax that is influenced by the `C` family of programming languages, but with a simplified syntax and less
cluttered appearance. Some of the key features of Go's syntax include:

#### Blocks and Statements

Like other C-style languages, Go uses curly braces to enclose blocks of code. Statements in Go are typically terminated
with a semicolon `;`, but they can also be automatically inferred by the compiler based on line breaks.

```
if x > 0 {
fmt.Println("x is positive")
}
```

#### Functions

Functions in Go are defined using the `func` keyword, followed by the function name, parameter list, and return type (if
any). Functions can return multiple values, which is a feature not commonly found in other programming languages.

```
func add(x int, y int) int {
return x + y
}

func swap(x, y string) (string, string) {
return y, x
}
```

#### Control Structures

Go has a variety of control structures that allow for conditional execution of code, including `if`/`else`
statements, `for` `loops`, and `switch` statements. The `defer` keyword can be used to schedule a function call to be
executed after the current function returns.

```go
package main

import (
	"fmt"
	"runtime"
)

func main() {
	var x int
	if x > 0 {
		fmt.Println("x is positive")
	} else if x == 0 {
		fmt.Println("x is zero")
	} else {
		fmt.Println("x is negative")
	}

	for i := 0; i < 10; i++ {
		fmt.Println(i)
	}

	switch os := runtime.GOOS; os {
	case "darwin":
		fmt.Println("OS X.")
	case "linux":
		fmt.Println("Linux.")
	default:
		fmt.Printf("%s.", os)
	}

	defer fmt.Println("world")

	fmt.Println("hello")
}
```

`Control structures` will be described in more detail later.

#### Pointers

In Go, pointers are used to reference a memory address of a value rather than the value itself. Pointers are declared
using the * operator, and the address of a variable can be obtained using the & operator.

```go
package main

import "fmt"

func main() {
	x := 10
	y := &x
	fmt.Println(*y) // prints 10
}
```

`Pointers` will be described in more detail later.

#### Structs

Structs in Go are similar to classes in other object-oriented programming languages, but they are much simpler and more
lightweight. Structs can contain fields (like class variables) and methods (like class functions).

```go
package smapleOne

import "fmt"

type Person struct {
	Name string
	Age  int
}

func (p *Person) SayHello() {
	fmt.Printf("Hello, my name is %s and I'm %d years old.\n", p.Name, p.Age)
}

func main() {
	p := &Person{"John", 30}
	p.SayHello() // prints "Hello, my name is John and I'm 30 years old."
}
```

`Structs` and `methods` will be described in more detail later.

#### Interfaces

Interfaces in Go are used to define a set of methods that a type must implement in order to be considered an
implementation of the interface. This allows for polymorphism and more flexible code.

```go
package main

import "fmt"

type Animal interface {
	Speak() string
}

type Dog struct {
	Name string
}

func (d *Dog) Speak() string {
	return "Woof!"
}

type Cat struct {
	Name string
}

func (c *Cat) Speak() string {
	return "Meow!"
}

func main() {
	animals := []Animal{
		&Dog{"Fido"},
		&Cat{"Fluffy"},
	}
	for _, animal := range animals {
		fmt.Println(animal.Speak())
	}
}
```

### Code comments

In Go, comments are used to provide additional information about the code to other developers. There are two types of
comments in Go: single-line comments and multi-line comments.

Single-line comments start with two forward slashes `//` and continue until the end of the line. For example:

```
// This is a single-line comment.
```

Multi-line comments start with a forward slash followed by an asterisk `/*` and end with an asterisk followed by a
forward slash `*/`. For example:

```
/*
   This is a multi-line comment.
   It can span multiple lines.
*/
```

When writing comments, it is important to follow some rules:

Comments should be used to explain the code, not to repeat it. For example, instead of
writing `// x = x + 1 : increment x`, it is better to write `// Increment x`.
Comments should be clear and concise.
Comments should be kept up-to-date with the code they describe. If the code changes, the comments should be updated as
well.

Using comments effectively can help make your code more readable and understandable for other developers.

### Statements

In Go, a statement is a unit of code that performs an action, such as declaring a variable, assigning a value to a
variable, or calling a function.

Here are some examples of statements in Go:

```go
package main

import "fmt"

func main() {

	// declaring a variable
	var x int

	// assigning a value to a variable
	x = 5

	// declaring and initializing a variable
	var y int = 10

	// calling a function
	fmt.Println("Hello, world!")

	// if statement
	if x > y {
		fmt.Println("x is greater than y")
	} else {
		fmt.Println("y is greater than or equal to x")
	}

	// for loop
	for i := 0; i < 10; i++ {
		fmt.Println(i)
	}

	// switch statement
	switch x {
	case 1:
		fmt.Println("x is 1")
	case 2:
		fmt.Println("x is 2")
	default:
		fmt.Println("x is not 1 or 2")
	}
}
```

### Packages

In Go, a `package` is a way of organizing and reusing code. A `package` can contain any number of Go source files, and
each source file can contain any number of functions, types, and variables.

When writing Go code, it is common to organize related functionality into separate packages. This allows the code to be
more modular, easier to maintain, and easier to reuse in other projects.

Go has a number of built-in packages that provide common functionality, such as fmt for formatting and printing output,
os for working with the operating system, and http for building web applications.

To use a `package` in Go, you need to first `import` it into your code. The syntax for importing a package is:

```
import "package-name"
```

For example, to use the `fmt` package to print output to the console, you would import it like this:

```
import "fmt"
```

Once you have imported a package, you can use its functions and types by prefixing them with the package name. For
example, to use the Println function from the fmt package, you would call it like this:

```
fmt.Println("Hello, World!")
```

In addition to using built-in packages, you can also create your own packages to organize your code. To create a new
package, you simply need to create a new directory with the package name and add one or more .go files to it.

For example, if you wanted to create a package called `myutil` that contains some utility functions, you could create a
directory structure like this:

```
myutil/
   |- util.go
```

The contents of `util.go` might look something like this:

```go
package myutil

func Add(a, b int) int {
	return a + b
}

func Subtract(a, b int) int {
	return a - b
}
```

You could then use this package in another Go program by importing it and using its functions:

```go
package main

import (
	"fmt"
	"myutil"
)

func main() {
	fmt.Println(myutil.Add(1, 2))
	fmt.Println(myutil.Subtract(3, 2))
}
```

This would output:

```
3
1
```

In summary, packages are a fundamental concept in Go that allow you to organize and reuse code. Go provides many
built-in packages for common functionality, and you can also create your own packages to organize your own code.