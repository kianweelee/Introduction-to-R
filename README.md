# Basics syntax and data types

## Understanding basic syntax

### Assigning data to variables
There are a few ways you can assign data to a variable:
1. ```->``` Right hand assignments
2. ```<-``` Left hand assignments
3. ```=``` Left hand assignments

### Print statements
Print statements are essential in coding and you will often see yourself using them.
```R
print("Hello beautiful people of the internet!")
```
Do note that we have embrace the sentence between double quotations ```"``` ```"```.
The main reason for that is that we are printing characters. If we are printing number, we will not need to use double quotations.
```R
print(1)
```

### Addition, subtraction, multiplication, division and remainders
1. Addition 
```R
print(1+1)
```
2. Subtraction
```R
print(2-1)
```
3. Multiplication
```R
print(1*3)
```
4. Division
```R
print(8/2)
```
5. Remainder
Here, we want to identify the remainder after we divide. For eg, when we divide 3 by 2, we will get a remainder of 1.
This method is also a great way for us to see if this number is divisible by for eg, 12 or if this number is odd or even.
```R
# Check if a number is even
print(8 %% 2)
``` 
This returns 0 as 8 is divisible by 2. 

```R
# When a number gets a remainder after division.
print( 3 %% 2)
```
    Output: 1
    
## Data types
There are 5 main data types, some of which you will not often use.
1. Character
2. Numeric (integer and double)
3. Logical
4. Complex number
5. Raw

### Character
Characters are often classified when you put them between 2 quotations. Same applies when you put a number between 2 quotations, which in turn convert it to character.

### Numeric
1. Interger and double (decimals)
2. Real number

### Logical 
1. TRUE
2. FALSE
3. NA

### Complex number
1. Contains imaginary number, ```i```

### Raw
1. Able to convert a character or numeric to bytes.
