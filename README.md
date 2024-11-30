# Keyboard Package

![Go Version](https://img.shields.io/badge/go-v1.23-blue)
![License](https://img.shields.io/badge/license-MIT-yellow)

## Description

The `keyboard` package provides a utility to read and parse floating-point numbers from standard input in a simple and reliable way. Ideal for command-line applications where user input is required.

---

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Examples](#examples)
- [Contributions](#contributions)
- [License](#license)

---

## Installation

To install the `keyboard` package, run the following command:

```bash
go get github.com/omarx/keyboard
```

---

## Usage

The `keyboard` package includes a single utility function, `GetFloat`, which reads input from the keyboard, trims unnecessary whitespace, and converts the input into a `float64`.

Here’s how to use it:

```go
package main

import (
	"fmt"
	"log"
	"keyboard"
)

func main() {
	fmt.Print("Enter a floating-point number: ")

	number, err := keyboard.GetFloat()
	if err != nil {
		log.Fatalf("Error reading input: %v", err)
	}

	fmt.Printf("You entered: %f\n", number)
}
```

---

## Features

- Reads input directly from the keyboard.
- Trims extra spaces or newlines from input.
- Parses input into a `float64`.
- Handles invalid input with meaningful error messages.

---

## Examples

### Basic Example

The following example demonstrates how to read and print a floating-point number:

```go
package main

import (
	"fmt"
	"log"
	"keyboard"
)

func main() {
	fmt.Print("Enter a floating-point number: ")

	number, err := keyboard.GetFloat()
	if err != nil {
		fmt.Println("Invalid input. Please enter a valid number.")
	} else {
		fmt.Printf("You entered: %f\n", number)
	}
}
```

### Handling Errors

```go
number, err := keyboard.GetFloat()
if err != nil {
    fmt.Println("Error reading input:", err)
} else {
    fmt.Printf("You entered: %f\n", number)
}
```

---

## Contributions

Contributions, bug reports, and feature requests are welcome!

To contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/my-feature`).
3. Commit your changes (`git commit -m 'Add feature'`).
4. Push to the branch (`git push origin feature/my-feature`).
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---