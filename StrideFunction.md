# Stride Function
## 1. What for:

Stride - is a function in Swift used to iterate over a given scope of numbers, for example "from: 1, to: 100", or, "from: 1, through: 100", we also use "by:" to specify the step of our stride.

## 2. Syntax:

The way we write stride function is very simple:

    stride(from: 0, to: 100, by: 1)

In this example we use "stride" to initialize the function, then we open parenthesis to set parameters for the function.

First we use `from` to specify thee beginning of our count.
Then we use either `to` or `through` to specify the point on which we end the count:

`to` - used to end the iterate excluding the end number (in our example, even though we've set ste function to go **from** 0 **to** 100, it would still finish at 99, giving us a scope of 0...99).
`through` - gives us the full scope of numbers **from** 0 **through** 100 (0..100)

We use a colon `:` after each parameter to specify it and a comma to separate each parameter.

## 3. Stride with Arrays and Variables

Interesting feature of a stride function is that we can iterate over an array or a variable.
In order to do that we would create a **for-in** loop that would take stride as a parameter. Inside stide in from parameter we would type the name of a variable/array and add **.startIndex**, in the example below we would see every other letter printed in the terminal.

  

     let letters = ["a", "b", "c", "d", "e", "f"]
    
                   for letter in stride(from: letters.startIndex, to: letters.endIndex, by: 2){
        print(letters[letter])
    }


Output:

    a
    c
    e

## 4. Iterating backwards
If we wanted to iterate backwards on a scope of 100...1, we could use an array with for-in loop in which we would reverse it.

    let numbers = Array(1...100)
    
    for num in numbers.reversed(){
        print(num)
    }

But instead we could utilize the stride function, since it would make the code simpler, more readable and performant:

    for number in stride(from: 100, through: 1, by: -1){
        print(number)


## More "by" examples
In this paragraph we will discuss how by parameter works more in-depth, since we could not only use "1", "-1" but also stride with wider leaps. 
Lets say we need to output numbers 0...100 going up by 10.
In this case we could use:

    for numbers in 0...10{
        print(numbers * 10)
    }

*Note how we multiply numbers within the print function, doing it before and outputting numbers separately would result in code outputting 0...10 instead of 0...100 by 10.

To simplify this code and make it more understandable we will use stride!
Here's how the code will look:

    for num in stride(from: 0, through: 100, by: 10){
        print(num)
    }


Notice how we go from 0 **through** 100 by increments of 10 and then simply print the result!

