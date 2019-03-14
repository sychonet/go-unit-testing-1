# Guidelines to write test cases in GoLang #

- - - - 

## Golang test function characteristics ##
* The first and only parameter needs to be `t *testing.T`
* It begins with the word `Test` followed by a word or phrase starting with a capital letter.(Example: TestValidateClient)
* Calls `t.Error` or `t.Fail` to indicate a failure (I called `t.Errorf` to provide more details)
* `t.Log` can be used to provide non-failing debug information
* Must be saved in a file named `something_test.go`

## References ##
