# Set Operations
## 1. Reminder: creating a set

In this bit we will quickly go through on how to create sets and then we will take a look on how to manipulate them. Creating an unpopulated set:

    var emptySet = Set<String>()
Creating a populated set:

    var populatedSet: Set = ["Tomato", "Cucumber"]

## 2. Inserting:

In the example above we have a populated set which contains two vegetables. In order to populate an empty set with fruits we will use the **.insert** method, in which we write our set name, add **.insert** at the end of it, open parenthesis, write, for example, **"Banana"** and here we go:

    emptySet.insert("Banana")

We can only add one value per insert,  meaning after adding orange our code will look something like this:

    var emptySet = Set<String>()
    
    emptySet.insert("Banana")
    emptySet.insert("Orange")
    
    print(emptySet)
The output for this code will look something like this:

    ["Orange", "Banana"]
Since sets are unorganized the output will differ from run to run.
## 3. Removing

In order to remove a value from the set we will use the **.remove** method which has a similar syntax, but this time we type in the value we want ro remove as oppose to adding one.

    emptySet.remove("Orange")
In the case above we removed Orange from the values of the set, so this time we print it out we get:

    ["Banana"]
Just a Banana.
## 4. Remove All
If we wanted to remove every value from the set, we could just use a method called **.removeAll** which uses the same syntax, again, but doesn't require any input.

    emptySet.removeAll()
After this line the set returns:

    []

## 5. Contains
Contains method returns a boolean result showing us whether the given value exists within the set:

    print(emptySet.contains("Orange"))
In this case we put .contains method inside the print function to return our result in terminal, which outputs us with:

    false
## 5. Count the amount of values
We will use .count method to count the amount of values inside the set as an integer.

    print(emptySet.count)
Here's **.count** method compared with a loop method that adds +1 to the total number in "count".

    var count = 0
    
    for _ in emptySet{
      count += 1
    }
    print(count)
    
    print(emptySet.count)

Both will return 0 since we do not have any more values in our set:

    0
## 6. Is Empty?
**.isEmpty** is a method which returns whether the set is empty of populated by returning a boolean result as an answer:

    print(emptySet.isEmpty)
Ironically, our emptySet in indeed empty, since the result is:

    true
## 6. Combining two sets together
Using **.union** we can combine values of two (or more) sets together but not the ones that repeat since sets only hold unique items. In order to use **.union** we will create a new set to which we will assign our combining operation.

    var thirdSet: Set = populatedSet.union(emptySet)
If we delete our removal operations from the emptySet. the output will look something like this:

    ["Cucumber", "Tomato", "Banana", "Orange"]
Now, lets create a third set called "superSet" for no reason and try to unite 3 at the same time.

    var superSet: Set = ["Pasta", "Cheese"]
Combination:

    var thirdSet: Set = populatedSet.union(emptySet).union(superSet)
Not let's take a look at the output:

    ["Pasta", "Cheese", "Cucumber", "Banana", "Orange", "Tomato"]
    
## 7. Intersection
Intersection is one of the easiest parameters, it outputs values which repeat in both sets.
**.intersection - outputs same items found in two sets.**
Let's take a look at a simple code with 3 sets that we will manipulate:

    var set1: Set = ["Tomato", "Carrot"]
    var set2: Set = ["Tomato", "Orange"]
    
    var set3: Set = set1.intersection(set2)
    print(set3)
In this code we've created 2 sets with repeating String of **"Tomato"**, after utilizing .intersection in the 3rd set we get the following output:

    ["Tomato"]
## 7. symetricDifference 
symetricDifference is a parameter that is complete opposite of .intersection, it returns the values that don't repeat in both sets.
**.symetricDifference - outputs items that are different in both sets (opposite of .intersection).**
Let's edit our previous code to demonstrate how it works:

    var set1: Set = ["Tomato", "Carrot"]
    var set2: Set = ["Tomato", "Orange"]
    
    var set3: Set = set1.symmetricDifference(set2)
    print(set3)
The output we get will look the following way:

    ["Carrot", "Orange"]
## 8. Subtracting  
Subtracting is used to subtract values of subtracting set from a subtracted one. Or simply:
**.subtracting - removes items found in the second set from the first.** 
The edited code:

    var set1: Set = ["Tomato", "Carrot"]
    var set2: Set = ["Tomato", "Orange"]
    
    var set3: Set = set1.subtracting(set2)
    print(set3)
Output:

    ["Carrot"]
The logic reminds of symetricDifference parameter, except in this case different values from the 2nd set aren't displayed.

## Notes
.insert
.remove
.removeAll
.contains - checks whether a set contains one specific item 
.count - counts how many items there are in sets as an integer
.isEmpty - literally checks if the set is empty, outputs a boolean result


.union - combines items of two sets together but not the ones that repeat since sets only hold unique items

.intersection - outputs same items found in two sets
.symetricDifference - outputs items that are different in both sets (opposite of .intersection)



.subtracting - removes items found in the second set from the first 

