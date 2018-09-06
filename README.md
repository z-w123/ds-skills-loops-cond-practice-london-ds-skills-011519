
# Loops Review


```python
for i in range(5):
    print(i, i**2)
```

    0 0
    1 1
    2 4
    3 9
    4 16


### Brief Notes
Notice above that we used `for i in range(5)` which includes 5 elements but starts with 0 and ends with 4.   
If we wanted the numbers 1 through 5 we would instead use the loop `for i in range(1,6)`.

# Booleans and Conditionals Review

## A simple example


```python
print('This is the start of the program.')
print('This is the start of iteration.')
for i in range(12):
    #This is the start of the for loop.
    print('i is: {}'.format(i)) #This happens every iteration
    
    if i % 2 == 0:
        print('i is even')
    elif i in [3,5,7,11]:
        print('i is prime!')
    elif i == 4:
        print('i is 4') #This will never actually happen because the conditional terminates since 4 is also even
    else:
        print('i is odd, but not prime')
    
    print('\n') #This is outside both conditional blocks. This happens once per iteration
    #Iteration completes, program returns to start of iteration block.
print('For loop complete.')
print('Script complete.')
```

    This is the start of the program.
    This is the start of iteration.
    i is: 0
    i is even
    
    
    i is: 1
    i is odd, but not prime
    
    
    i is: 2
    i is even
    
    
    i is: 3
    i is prime!
    
    
    i is: 4
    i is even
    
    
    i is: 5
    i is prime!
    
    
    i is: 6
    i is even
    
    
    i is: 7
    i is prime!
    
    
    i is: 8
    i is even
    
    
    i is: 9
    i is odd, but not prime
    
    
    i is: 10
    i is even
    
    
    i is: 11
    i is prime!
    
    
    For loop complete.
    Script complete.


### Brief notes
Notice the common conditional `i % 2 == 0` which is used to determine if a number is even (or odd). Recall that the `%` operator returns the remainder when dividing i by 2. Equivalently, this is i mod 2.  

Also note that the second elif clause `elif i == 4` is never executed because the conditional block completes as soon as a clause is true. In the below example, we examine how multiple conditional blocks can be chained.  

Another style that can be explored is combining multiple conditions such as `if i > 5 and i < 10:` or `if i == 7 or i > 8:`. In general, combining statements such as this should be used as opposed to nesting conditional blocks within each other which can become difficult to read. For example: 


```python
for i in range(50):
    if i >5:
        #Works but cautionary style. Often can become difficult to read. Do not overnest conditionals.
        if i < 10:
            print(i)#to be executed
```

    6
    7
    8
    9


## A complex example


```python
print('This is the start of the program.')
print('This is the start of iteration.')
for i in range(12):
    #This is the start of the for loop.
    print('i is: {}'.format(i)) #This happens every iteration
    print('This is the first condition block.')
    #This is the start of our conditional block
    if i < 6:
        print('i is less then 6') #This is inside the 'if i < 6 condition'
    elif i % 2 == 0:
        print('i is even') #This is inside the 'elif i % 2 == 0 condition'
        print('this statement only executes if the if condition above (i<6) is false.')
        #The elif condition is only reached if the preceeding if statement is false.
        #Once one of the branches is triggered, the program exits this entire conditional block
    elif i == 7:
        print('i is 7!')
    else:
        print('Bigger then 7, and odd')
    #End of first conditional block
    
    #Start of second conditional block
    print('This is the second condition block.')
    if i % 2 == 0:
        print('i is even')
    else:
        print('i is odd')
    #End of second contional block
    
    print('\n') #This is outside both conditional blocks. This happens once per iteration
    #Iteration completes, program returns to start of iteration block.
print('For loop complete.')
print('Script complete.')
```

    This is the start of the program.
    This is the start of iteration.
    i is: 0
    This is the first condition block.
    i is less then 6
    This is the second condition block.
    i is even
    
    
    i is: 1
    This is the first condition block.
    i is less then 6
    This is the second condition block.
    i is odd
    
    
    i is: 2
    This is the first condition block.
    i is less then 6
    This is the second condition block.
    i is even
    
    
    i is: 3
    This is the first condition block.
    i is less then 6
    This is the second condition block.
    i is odd
    
    
    i is: 4
    This is the first condition block.
    i is less then 6
    This is the second condition block.
    i is even
    
    
    i is: 5
    This is the first condition block.
    i is less then 6
    This is the second condition block.
    i is odd
    
    
    i is: 6
    This is the first condition block.
    i is even
    this statement only executes if the if condition above (i<6) is false.
    This is the second condition block.
    i is even
    
    
    i is: 7
    This is the first condition block.
    i is 7!
    This is the second condition block.
    i is odd
    
    
    i is: 8
    This is the first condition block.
    i is even
    this statement only executes if the if condition above (i<6) is false.
    This is the second condition block.
    i is even
    
    
    i is: 9
    This is the first condition block.
    Bigger then 7, and odd
    This is the second condition block.
    i is odd
    
    
    i is: 10
    This is the first condition block.
    i is even
    this statement only executes if the if condition above (i<6) is false.
    This is the second condition block.
    i is even
    
    
    i is: 11
    This is the first condition block.
    Bigger then 7, and odd
    This is the second condition block.
    i is odd
    
    
    For loop complete.
    Script complete.


# Biz Buzz Bop
You can quickly generate a list of numbers by using the range function. Use a for loop to iterate through the numbers 1 to 100, inclusive, print the number n, along with the following conditional actions:

* If  n is odd, print ‘is odd’
* If  n is even and divisible by 7, print ‘is divisible by 14’
* If  n is divisible by 5, but not even, print ‘high five!’
* If  n is greater than 30, less then 45 and divisible by 8, print ‘this happens twice!’


```python
# Your code here
```

# Extension
Write a condition to determine if the number is prime.


```python
# Your code here
```
