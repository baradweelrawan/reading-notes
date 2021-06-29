# this is read09 from 301
# Concepts of Functional Programming in Javascript

![img](https://miro.medium.com/max/800/1*JyVlvqwsCBYl2FuvPFVRZQ.png)

# What is functional programming?
It's a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data .Why is this an impure function?Simply because it uses a global object that was not passed as a parameter to the function.

# Random number generation:
Any function that relies on a random number generator cannot be pure.Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen.

# Pure functions benefits :
  1. Given a parameter A → expect the function to return value B.
  2. Given a parameter C → expect the function to return value D.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.In Javascript we commonly use the for loop. This next for statement has some mutable variables.It is also very common to build up the final state of an object. Imagine we have a string, and we want to transform this string into a url slug.

# function composition, or function chaining :
the result of a function will be used as an input for the next function, without modifying the original input string.
   1. toLowerCase: converts the string to all lower case.
   2. trim: removes whitespace from both ends of a string.
   3. split and join: replaces all instances of match with replacement in a given string.
   4. To combine all these 4 functions and we can "slugify" our string.

pure functions + immutable data = referential transparency;With this concept, a cool thing we can do is to memoize the function.

# Functions as first-class entities :
The idea of functions as first-class entities is that functions are also treated as values and used as data.Functions as first-class entities can:
   1. refer to it from constants and variables.
   2. pass it as a parameter to other functions.
   3. return it as result from other functions .
The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.

# Higher-order functions :
we mean a function that either;takes one or more functions as arguments, or returns a function as its result.The doubleOperator function we implemented above is a higher-order function because it takes an operator function as an argument and uses it.

# Filter :
Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.

# Map :
The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.The idea of map is to transform a collection.Another interesting Hacker Rank problem was the update list problem. We just want to update the values of a given array with their absolute values.We use the Math.abs function to transform the value into its absolute value, and do the in-place update.
   * The first idea was to test the Math.abs function to handle only one value.

# Reduce :
The idea of reduce is to receive a function and a collection, and return a value created by combining the items.

   


















  




