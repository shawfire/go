# go

[golang online repl and reference](https://golang.org/)
Code in the online repl runs in a sanbox, same time, no web server or file access.

[golang download page](https://golang.org/dl/)

Once installed try it out:
```
$ go run palindrome.go
A Palindrome
************
aibohphobia
$ go run stars.go
*
**
***
****
*****
$
```

## Golang systax rules:
+ Golang is compiled statically type, with no inheritance but does support interfaces. 
+ Go is case sensitive and has minimal syntaxs and reserved words. 
```
var fruits [2]string
fruits[0] = "Apple"
fruits[1] = "Orrange"
```
+ Variables ang pakage names are lower and mixed case. 
+ Exported functions and fields are capitalized (which means they have an application scope).
+ Line feed ends a statement; no semicolon is required.
+ Semicolons are part of the formal language spec; however the lexer add them as needed.
+ Code blocks are wrapped with braces, with the starting brace on the same line as preceding statement:
	for i := 0; i < 5; i++ {
		for j := 0; j <= i; j++ {
			fmt.Print("*")
		}
		fmt.Println("")
	}
+ built-in functions and members of builtin package [reference](http://golang.org/pkg/builtin/):
len(string) - return the length of a string as in python
panic(error) - stops execution and displays error message
recover() - manages behavior of a panicking goroutine

## Go command line - create an executable (on a mac)
+ Documentation 
```
$ godoc
$ godoc fmt
$ gofmt -w palindrome.go
$ go
$ go run palindrome.go
$ go build
$ go install
$ mkdir my_project
$ cd my_project
$ mkdir src
$ mkdir bin
$ mkdir pkg
$ export GOPATH=~/dev/go/my_project
$ go env
$ cd src
$ mkdir palindrome
$ cd !$
$ cp ../../../palindrome.go  .
$ go install
$ cd ../../bin
$ ./palindrome
```
[Package names](https://blog.golang.org/package-names)

## Main, library and tests.
[Golang project and testing](https://golang.org/doc/code.html)
```
$ cd $GOPATH
$ $GOPATH/bin/hello
Hello, Go!
$ cd $GOPATH/src/stringutil/
$ go build
$ go test
PASS
ok      stringutil      0.006s
$
```
