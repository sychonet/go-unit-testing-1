# Guidelines to write test cases in Go #

- - - - 

## Go test function characteristics ##
* The first and only parameter needs to be `t *testing.T`
* It begins with the word `Test` followed by a word or phrase starting with a capital letter.(Example: TestValidateClient)
* Calls `t.Error` or `t.Fail` to indicate a failure
* `t.Log` can be used to provide non-failing debug information
* Must be saved in a file named `something_test.go`. NOTE: Go compiler and linker will not ship your test files in any binaries it produces.

## Launching Tests ##
There are two ways to launch tests for a package:
1. Within the same directory as the test `$ go test -v`. NOTE: This picks up any files matching packagename_test.go
2. By fully-qualified package name `$ go test github.com/alexellis/golangbasics1`  

These methods work for unit tests and integration tests alike.

## Statement coverage in tests ##
The go test tool has built-in code-coverage for statements.
`$ go test -cover`

## Generating HTML coverage report ##
`$ go test -cover -coverprofile=c.out`
`$ go tool cover -html=c.out -o coverage.html`

## References ##
* https://blog.alexellis.io/golang-writing-unit-tests/