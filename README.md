# R Objects - Vectors and Lists

## What is an R object?
They are common data structures that has its own methods and attributes.

## Types of R objects
1. Vectors
2. Lists
3. Matrices
4. Factors
5. Dataframe

## Vectors
- Most common data structure used.
- Can only contain a single data type in it.
- Data wrapped in c()
- Example: 
  * ```df <- c(1,2,3)``` for intergers type
  * ```df <- c('a', 'b', 'c')``` for character type
  * ```df <- c(TRUE, FALSE)``` for logical type

### What if we decides to mix integer with characters?
```R
df <- c('A', 1,2)
```
    output: [1] 'A' '1' '2'

All will be automatically converted to character type.
All convertion is done from lower to higher types (logical -> integer -> double -> character).

### What if we decides to mix logical data with integer?
```R
df <- c(TRUE, 1,2)
```
    output: [1] 1 1 2

Do notice that TRUE and FALSE has an interger value of 1 and 0 respectively. Since integer is on a higher type than logical, it will be converted to integer.

### What if we decides to mix integer data with double data?
 ```R
 df <- c(1,2,9.8)
 ```
    output: [1] 1.0 2.0 9.8
 
 Since double is on a higher level than integer, integers will be converted to double data type (with decimals)
 
 ### Adding consecutive numbers into vectors 
 This can be done using ```:```.
 ```R
 df <- c(1:10)
 ```
    output: [1]  1  2  3  4  5  6  7  8  9 10
 
 ```R
 df1 <- c(-4:4)
 ```
    output: [1] -4 -3 -2 -1  0  1  2  3  4
 
This is assuming that the numbers are moving in an increment of 1. What if we want to adjust the step size?
Well, we will need to use ```seq(start, end, by = ...)``` where start is the first number of the sequence, end is the last number and by is the amount of step size needed.
 
```R
df <- c(seq(1,3,by = 0.5))
```
    output: [1] 1.0 1.5 2.0 2.5 3.0

### Access item from vector
- Lets say if we want to access the first item. We can:

```R
df <- c(1:10)
df[1]
```
- Access first and fifth item:

```R
df[c(1,5)]
```

### Editing the item in a vector
We can edit the item by identifying the index of the item and reassigning the new data into it.
For example, if we want to change the 4th index of df from ```4``` to ```44```, we can:
```R
df[4] <- 44
```

### Deleting a vector
We can delete a vector by assigning it with a ```NULL``` value.
```R
df <- c(1:10)
df <- NULL
df
```
    output: NULL
    
## Lists
- Similar to vector but can store multiple data types as oppose to only one in vector.
- List can be created using the ```list()``` syntax.

Example:
```R
df <- list('A', TRUE, 1, 1.1)
df
```
```
  [[1]]
  [1] "A"

  [[2]]
  [1] TRUE

  [[3]]
  [1] 1

  [[4]]
  [1] 1.1
```
### Searching for items in a list
To search, we can use index to find the items.

```R
df1 <- list(c('A','B'), 2, TRUE)
df1
```
```
[[1]]
[1] "A" "B"

[[2]]
[1] 2

[[3]]
[1] TRUE
```
Notice that the first index is in between ```[[]]```? When we reference the list, instead of indexing the first element as ```[1]```, we do it as ```[[1]]```.

So to find the first item in the list, we use ```df1[[1]]```. But what if we want to find "A"? Well, we can do ```df1[[1]][1]``` for "A" and ```df1[[1]][2]``` for "B".

### Modifying items in a list
```R
df1 <- list(c('A','B'), 2, TRUE)
df1
```
```
[[1]]
[1] "A" "B"

[[2]]
[1] 2

[[3]]
[1] TRUE
```
Lets say we want to modify the first index and change "B" to "C".
We can:

```R
df1[[1]][2] <- "C"
```

### Deleting components from a list
Similar to vectors, we can assign ```NULL``` to the index.
For example if we want to remove the first index containing a vector of "A" and "B":

```R
df1[[1]] <- NULL
```
