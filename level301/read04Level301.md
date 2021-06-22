# this is read04 from 301
# React: Forms
![img](https://i.ytimg.com/vi/t3r9xW-sxqs/maxresdefault.jpg)

TML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state. it’s convenient to have a JavaScript function that handles the submission of the form and has access to the data that the user entered into the form. The standard way to achieve this is with a technique called “controlled components”.

# Controlled Components:
In React, mutable state is typically kept in the state property of components, and only updated with setState().you can combine the two by making the React state be the single source of truth. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a controlled component.With a controlled component, the input’s value is always driven by the React state. While this means you have to type a bit more code, you can now pass the value to other UI elements too, or reset it from other event handlers.

# The textarea Tag :
In React, a <textarea> uses a value attribute instead. This way, a form using a <textarea> can be written very similarly to a form that uses a single-line input.the this.state.value is initialized in the constructor, so that the text area starts off with some text in it.

# The select Tag :
In HTML, <select> creates a drop-down list.React, instead of using this selected attribute, uses a value attribute on the root select tag. This is more convenient in a controlled component because you only need to update it in one place.this makes it so that <input type="text">, <textarea>, and <select> all work very similarly - they all accept a value attribute that you can use to implement a controlled component.

# The file input Tag :
n HTML, an <input type="file"> lets the user choose one or more files from their device storage to be uploaded to a server or manipulated by JavaScript via the File API.in React its value is read-only, it is an uncontrolled component.

# Handling Multiple Inputs :
When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.Also, since setState() automatically merges a partial state into the current state, we only needed to call it with the changed parts.

# Controlled Input Null Value :
Specifying the value prop on a controlled component prevents the user from changing the input unless you desire so. If you’ve specified a value but the input is still editable, you may have accidentally set value to undefined or null.

# Fully-Fledged Solutions :
If you’re looking for a complete solution including validation, keeping track of the visited fields, and handling form submission, Formik is one of the popular choices. However, it is built on the same principles of controlled components and managing state .










