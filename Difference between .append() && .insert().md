# Difference between .append() && .insert()
## 1. .append() in Arrays
As the word meaning says:

> Append - add (something) to the end of a written document.

So, following the definition we understand that append adds a value to the end of an Array or a Set (more on sets later).
So if we create an Array using the following code:

    var arrayForTest: Array = ["Carrot", "Onion"]
**Remember? Arrays are an ordered collection of values.**

So if we wanted to add "Milk" into our new array we would write our variable's name followed by an .append() operator, adding our value in parenthesis.

    arrayForTest.append("Milk")
If we run the program now we will get the following output:

    ["Carrot", "Onion", "Milk"]
## 2. .append() in Sets
Nope, we cannot use .append with sets.
**Remember? Sets are unordered collections of unique values.**
This means if we were to change our code to look something like this:

    var setForTest: Set = ["Carrot", "Onion"]
    setForTest.append("Milk")
It would output an error in the therminal saying:

    expression failed to parse:
    error: MyPlaygroundAppendInsert.playground:11:12: error: value of type 'Set<String>' has no member 'append'
    setForTest.append("Milk")
    ~~~~~~~~~~ ^~~~~~

**value of type 'Set<String>' has no member 'append'**

We cannot add a value at the end of our set since set doesn't have an end at all.

## 3. .insert(value, at: Int) in Arrays
.insert parameter allows us to inset a value into an array not only at the end but in any place we want, ranging from 0 and futher. 
**Remember? The first value in sets, arrays etc. in Swift doesn't go by a number of 1, all the count starts from 0, so the first value is always positioned at 0.** 
In this example we add "Cabbage" to the middle of the array using the the syntax:

    nameOfTheArray.insert("Value", at: Int)
So now our code will look as follows:

    var arrayForTest: Array = ["Carrot", "Onion"]
    arrayForTest.insert("Cabbage", at: 1)
    print(arrayForTest)
    
Output result:

    ["Carrot", "Cabbage", "Onion"]
Just what we expected, "Cabbage" in the middle!

## 4. .insert(value) in Sets
The same parameter .insert() can also be used for sets as well, finally. But it's not over, there is a minor difference to note, since sets are unorganized collections of values, then we don't need to specify at: what position do we want to insert a value, we just insert it and that's it!
So if we try to specify at what Int we want our insert to occur:

    var setForTest: Set = ["Carrot", "Onion"]
    setForTest.insert("Watermelon", at: 1)
    print(setForTest)
We will get the following error:

    expression failed to parse:
    error: MyPlaygroundAppendInsert.playground:12:37: error: extra argument 'at' in call
    setForTest.insert("Watermelon", at: 1)
                     ~~~~~~~~~~~~~~~~~~~^~


**extra argument 'at' in call**
So we don't use at: argument for inserts for Sets, instead our fixed code should look like this:

    var setForTest: Set = ["Carrot", "Onion"]
    setForTest.insert("Watermelon")
    print(setForTest)
And our output will be a set of values, including our new value "Watermelon" in a random order:

    ["Watermelon", "Carrot", "Onion"]

**Thanks for attention!**

