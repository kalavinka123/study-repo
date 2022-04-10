# Setting up the environment
Open up the extention tab of VS code and download GO package.  
Then, change the language mode from plain text to Go.  
<img src="https://user-images.githubusercontent.com/48580911/162607649-8c9baf8b-b863-4605-9af1-08c369fb8d06.jpg" width=50% height=50%>

# Run the Go program
### hello.go
```
package main

import "fmt"

func main() {
	fmt.Println("Hello World from GO!")
}
```
Type the following command from a terminal to run the code.
```
$ go run hello.go
Hello World from GO!
```

- go run : compile & execute immediately
- go build : just compile
```
# See the compiled file with the go build command
$ ll
total 1885
-rwxr-xr-x 1 kala 197121 1926144 Jan 20 22:43 hello.exe*

# Execute the compiled file.
$ ./hello.exe 
Hello World from GO!
```
- 
