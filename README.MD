# ESEP Grade Calculator

This project is a simple Go library for calculating a weighted final grade based on input assignments, exams, and essays.

## Tech Stack

- Programming Language: Go 1.24+
- Unit Tests: testing (Go's native testing package)

## Getting Started

### Setup

- Fork the main branch to your personal account
- Install Go 1.24+ as described in the [Go documentation](https://go.dev/doc/install).

### Using the Calculator

#### Supported Methods

Initialize a Calculator

```
NewGradeCalculator()
```

Add a grade

```
AddGrade(name string, grade int, gradeType GradeType)
```

Get final grade (calculated as a weighted average)

```
GetFinalGrade()
```

Here is a simple example showing how to import the calculator module, add grades, and calculate a final grade:

```
// example/main.go
package main

import calculator "esep/grade-calculator"
import "fmt"

func main() {
    gradeCalculator := calculator.NewGradeCalculator()
    gradeCalculator.AddGrade("open source assignment", 90, calculator.Assignment)
    gradeCalculator.AddGrade("exam 1", 95, calculator.Exam)
    gradeCalculator.AddGrade("essay on ai ethics", 91, calculator.Essay)

    final_grade := gradeCalculator.GetFinalGrade()
    fmt.Printf("Your final grade is: '%s'\n", final_grade)
}

```

### Running Unit Tests

Run unit tests without code coverage:

```
cd grade_calculator/
go test ./...
```

Run unit tests with code coverage:

```
cd grade_calculator/
go test -coverprofile=coverage.txt ./...
```

## Project Structure

- `go.mod` Go module definition
- `grade_calculator.go` Implements the classes and functions that carry out the functionality of a grade calculator.
- `grade_calculator_test.go` Defines unit tests that test the grade calculator functionality.
