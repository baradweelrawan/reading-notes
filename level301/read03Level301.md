# this is read03 from 301
# React: Lists and Keys
![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQYFYUMxwjoJUgk-Bv9mwUGhi6uhAIKOfWZHw&usqp=CAU)

we use the map() function to take an array of numbers and double their values. We assign the new array returned by map() to the variable doubled and log it.In React, transforming arrays into lists of elements is nearly identical.

# Rendering Multiple Components :
can build collections of elements and include them in JSX using curly braces {}.using the JavaScript map() function to loop through the array.then return an element for each item.and assign the resulting array of elements.

# Basic List Component :
Usually you would render lists inside a component.you can refactor the previous example into a component that accepts an array of numbers and outputs a list of elements.

# Keys :
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys.When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort.

# Extracting Components with Keys :
Keys only make sense in the context of the surrounding array.if you extract a ListItem component, you should keep the key on the <ListItem /> elements in the array rather than on the <li> element in the ListItem itself.A good rule of thumb is that elements inside the map() call need keys.

# Keys Must Only Be Unique Among Siblings
Keys serve as a hint to React but they don’t get passed to your components. If you need the same value in your component, pass it explicitly as a prop with a different name.Sometimes this results in clearer code, but this style can also be abused. 












