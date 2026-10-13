# ESEP Grade Calculator

This library is a simple utility to calculate a final letter grade from the following categories: assignment, exam, and essay.

Project structure:
```
README.MD
grade-calculator/
- go.mod                      // Go module definition
- grade_calculator.go         // GradeCalculator implementation
- grade_calculator_test.go    // Unit tests 
```

Runtime requirements:
Golang 1.24+

Usage(for example):
```
gc := NewGradeCalculator()
gc.AddGrade("open source assignment", 100, Assignment)
gc.AddGrade("exam 1", 95, Exam)
gc.AddGrade("essay on ai ethics", 91, Essay)
letter := gc.GetFinalGrade() // Output will be: "A", "B", "C", "D", or "F"
```
Current Grading Implementation:
Final score weighted: Assigments(50%), Exams(35%), Essays(15%)
Letter Grading: A(>=90), B(>=80), C(>=70), D(>=60), F(<60)

Run unit tests:
```
cd grade-calculator/
go test ./...
```

Run unit tests with code coverage:
```
cd grade-calculator/
go test -coverprofile=coverage.txt ./...
```
