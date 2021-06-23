# this is read04 from 301
# Thinking in React :

![img]https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQnMN_53Uo8psedFKMB9zbejdIzAY8vTEv6XQ&usqp=CAU)

React is the premier way to build big, fast Web apps with JavaScript. It has scaled very well for us at Facebook and Instagram.One of the many great parts of React is how it makes you think about apps as you build them. In this document, we’ll walk you through the thought process of building a searchable product data table using React.

# Start With A Mock :
magine that we already have a JSON API and a mock from our designer.
 1.  Break The UI Into A Component Hierarchy:The first thing you’ll want to do is to draw boxes around every component and subcomponent in the mock and give them all names.Use the same techniques for deciding if you should create a new function or object. One such technique is the single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.Since you’re often displaying a JSON data model to a user, you’ll find that if your model was built correctly, your UI and therefore your component structure will map nicely.Components that appear within another component in the mock should appear as a child in the hierarchy:(FilterableProductTable).

 2. Build A Static Version in React :
 The easiest way is to build a version that takes your data model and renders the UI but has no interactivity. It’s best to decouple these processes because building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing. To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props. props are a way of passing data from parent to child.At the end of this step, you’ll have a library of reusable components that render your data model. The components will only have render() methods since this is a static version of your app. The component at the top of the hierarchy (FilterableProductTable) will take your data model as a prop.

 3. Identify The Minimal (but complete) Representation Of UI State :
 To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state.To build your app correctly, you first need to think of the minimal set of mutable state that your app needs.

 4. Identify Where Your State Should Live :
 we need to identify which component mutates, or owns, this state.React is all about one-way data flow down the component hierarchy. It may not be immediately clear which component should own what state.For each piece of state in your application:

   * Identify every component that renders something based on that state.
   * Find a common owner component a single component above all the components that need the state in the hierarchy.
   * Either the common owner or another component higher up in the hierarchy should own the state.
   * If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

 5. Add Inverse Data Flow :
  it’s time to support data flowing the other way: the form components deep in the hierarchy need to update the state in FilterableProductTable.React makes this data flow explicit to help you understand how your program works, but it does require a little more typing than traditional two-way data binding.whenever the user changes the form, we update the state to reflect the user input. Since components should only update their own state, FilterableProductTable will pass callbacks to SearchBar that will fire whenever the state should be updated. We can use the onChange event on the inputs to be notified of it. The callbacks passed by FilterableProductTable will call setState(), and the app will be updated.  

 # A Brief Interlude: Props vs State :
 There are two types of “model” data in React: props and state. It’s important to understand the distinction between the two.


