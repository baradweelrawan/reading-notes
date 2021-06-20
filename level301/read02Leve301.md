# this is read02 from 301
# React: Component Lifecycle Events :
![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTuyb0pK5Djj5MW8CSvzJ6iZUZzzSdrfIAEwQ&usqp=CAU)

# What are component lifecycle events?
React lets you define components as classes or functions. The methods that you are able to use on these are called lifecycle events. These methods can be called during the lifecycle of a component, and they allow you to update the UI and application states.Mounting, Updating, and Unmounting are the three phases of the component lifecycle.

1. Mounting :
When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting.

2. Updating :
Anytime a component is updated or state changes then it is rerendered. These lifecycle events happen during updating in this order.

3. Unmounting :
The final phase of the lifecycle if called when a component is being removed from the DOM. componentWillUnmount is the only lifecycle event during this phase.

# constructor() :
The constructor for a React component is called before it is mounted.If the component is a subclass you should call super(props), or the props will be undefined. constructors can be used to assign state using this.state or to bind event handle methods to an instance.Avoid using this.setState() in the constructor because it can lead to side effects, and it is unnecessary. Doing this will ignore all updates to props, so it shouldn’t be done unless it is intentional.

# static getDerivedStateFromProps() :
This method exists for rare cases where the state relies on changes in props over time.

# render():
Render is the only required method in a class component. It will examine this.props and this.state when called. The render function should not modify the component state because it would cause a lot of bugs by changing the state every time it rerenders.

# componentDidMount() :
This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, and is a good place to set up any subscriptions. If you do that, don’t forget to unsubscribe in componentWillUnmount(). setState() can be called here, but it should be used sparingly, because it will cause a rerender, which can lead to perfomance issues.

# shouldComponentUpdate() :
The default behavior in react is to rerender after every state change. Setting shouldComponentUpdate() to false allows you to prevent this from happening. This is in order to optimize performance.

# getSnapshotBeforeUpdate() :
This is another rarely used method that allows you to capture a picture of the DOM to check it before actually changing anything on the DOM.

# componentDidUpdate() :
it is useful for performing network requests after a change has occurred.

# componentWillUnmount() :
it's allows you to clean up the DOM and netwrok requests/ subscriptions.

# allows you to clean up the DOM and netwrok requests/ subscriptions:
1. What is a Linked List?

![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRZJlbAu62T7NwA4jImZHHYpaofsSNtY1_xNw&usqp=CAU)

A linked list is a linear data structure where each element is a separate object usually called a node.A node is comprised of the data and a reference to the next node. The last node has a reference to null. The head of the linked list is not a separate node. It is a reference to the first node. If the list is empty then the head is a null reference. This type of linked list is called a singly linked list.





