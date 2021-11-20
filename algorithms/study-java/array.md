## Array
### 1. Array Initializer
Use it when the size of the array and variables of array are already known.
```
int[] arr = {1, 2, 3};
```
or
```
int[] arr = null;
arr = new int[] {1, 2, 3}
```
:warning: It is not allowed to initialize an array with the curly braces once the array has been declared.
```
int[] arr = null;
arr = {1, 2, 3} // Compiler Error
```

### 2. length property
The length is property, not a method.
```
int[] arr = new int[10];
int size = arr.length;
// int size = arr.length();
```

### 3. Arrays Class Methods
https://docs.oracle.com/javase/8/docs/api/index.html   

Some of the methods often used are...
- asList()
- binarySearch()
- copyOf()
- copyOfRange()
- equals()
- deepEquals()
- fill()
- sort()
- paralleSort()
- spliterator()
- setAll()
- parallelSetAll()
- parallelPrefix()
- toString()
- deepToString()
