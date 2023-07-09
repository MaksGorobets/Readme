# Variables and data types
## 1. Declaring a variable:

There are two methods of declaring a variable in Swift: **var**, **let**.

In the first case we can use **var** to declare a variable that will hold some data that can later be modified. When declaring a variable we use **var**, then the name of the variable, for example **“name”** then we use  an assignment operator **“=“** to add something that our variable can contain.

    var name  = 123
That way we successfully created a variable that contains the number **“123”**. We can also specify which data type we are going to be using in our variable.

## 2. Basic data types:

Swift has 4 basic data types that we can assign to a variable, including:

`Int` - basic number, such as **“123”**
`Double` - floating point number **“123.10”**
`String` - any sentence or word **“Hello, world”**
`Character` - any ONE number or letter **“H”**, **“1”**

There is more but it’s a topic for another discussion.

## 3. Specifying a data type:

If we were to specify that our “123” is specifically an Integer, then the syntax would have looked like this:

    var name: Int = 123

We use **“:”** after a name of the variable to specify which data type we are going to be using, data type itself must always be written starting with a **capital letter**, then we use an assignment operator, as usual, to store the data into a variable.

## 4. Let

Let has the same syntax as a regular variable, with only exception that let cannot be modified throughout the execution, let variable is constant and won’t change after its initial declaration.

    let name: Int = 123


## Possible questions

In swift programming language we use : to specify which data type our variable will hold, but how is it useful if swift can identify which type of data our variable uses on it's own?

Well, it is usually better for readability and explicitness, we can also specify the data type in a variable to override any potential problems with a variable’s data type.



