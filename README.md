# Go (Golang) for Python developers 🚀
This project is inspired by the [Golang for Node.js developers](https://github.com/miguelmota/golang-for-nodejs-developers/) project. Similar to that project, I will do my best to provide numerous examples for those who are familiar with Python and are interested in learning Go.
Personally, my journey is similar to yours. I started with Python and later became drawn to this delightful and efficient language :) 

## Examples
---
### Variables
#### Python
```python
mutable_variable = 2
CONST_VARIABLE = 3.14 # There isn't a way to define a constant variable in Python

a, b = 1, "one" # Declaring two mutable variables at once
```

#### Go
```go
var mutableVariable int = 2
const ConstVariable float = 3.14

var a, b = 1, "one" // Go automatically assigns types to each variable (type inferred), so you can't change them later.
```
---

### Data Types
#### Python
```python
string_var = "Hello Python!"
integer_var = 2
float_var = 3.14
boolean_var = True
```

#### Go
```go
var string_var string = "Hello Go!"
var integer_var int = 2
var float_var float = 3.14
var boolean_var bool = true
```
---

### For loop
#### Python
```python
i = 10

for i in range(10):
    print(i)
```

#### Go
```go
// Initial; condition; after loop
for i := 0; i < 10; i++ { // Using the shorthand syntax of declaring a variable in Go (mutableVar := the value)
    fmt.Println(i)
}
```
---

### While loop
#### Python
```python
counter = 0

while counter < 5:
    print(counter)
    counter += 1
```

#### Go
```go
var counter int = 0

for counter < 5 {
    fmt.Println(counter)
    counter += 1
}
```
---

### If/Else
#### Python
```python
age = 25

if age >= 13 and age <= 19:
    print("Teenager")
elif age >= 20 and age <= 29:
    print("Young adult")
elif age >= 30 and age <= 39:
    print("Adult")
else:
    print("Other")
```

#### Go
```go
var age int = 25

if age >= 13 && age <= 19 {
    fmt.Println("Teenager")
} else if age >= 20 && age <= 29 {
    fmt.Println("Young adult")
} else if age >= 30 && age <= 39 {
    fmt.Println("Adult")
} else {
    fmt.Println("Other")
}
```
---

### Array/Slice
#### Python
```python
mix_list = [False, 1, "two"] # Can be any size
```

#### Go
```go
var boolArray [3]bool = [3]bool{false, true, true} // var variableName [array size]type of array elements
var stringArray [3]string = [3]string{"zero", "one", "two"}
var intArray [3]int = [3]int{0, 1, 2}

var boolSlice []bool = []bool{false} // var variableName []type of slice elements
var stringSlice []string = []string{"zero", "one"}
var intSlice []int = []int{0, 1, 2}
```
---

### For loop Over Array/Slice
#### Python
```python
mix_list = [False, 1, "two"]

for item in mix_list:
    print(item)
```

#### Go
```go
var intSlice []int = []int{0, 1, 2}
for index, value := range intSlice {
    fmt.Println(index, value)
}
```
---

### Map
Think of Map as Python's dictionary. Like an Array/Slice, it requires specifying key and value types.
#### Python
```python
the_dictionary = {"hi": 1, "bye": False}
print(the_dictionary["hi"])
```

#### Go
```go
var theMap map[string]int = map[string]int{"hi": 1, "bye": 0}
fmt.Println(theMap["hi"])
```
---

### Function
#### Python
```python
def the_function(first_arg, second_arg):
    return f"The first argument is {first_arg} and the second argument is {second_arg}", True
```

#### Go
```go
func theFunction(firstArg string, secondArg string) (string, bool) { // (argument argumentType) (return typeValue)
    return fmt.Sprintf("The first argument is %s and the second argument is %s", firstArg, secondArg), true
}
```
---

### HTTP Get Request
#### Python
```python
import requests

response = requests.get("https://example.com/")
print(response.content)
```

#### Go
```go
import (
    "fmt"
    "io"
    "log"
    "net/http"
)

resp, err := http.Get("https://example.com/")
if err != nil {
	log.Println(err)
}
defer resp.Body.Close()

body, err := io.ReadAll(resp.Body)
fmt.Println(string(body))
```
