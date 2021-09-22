## State vs Props
What types of things can you pass in the props?
information that is needed from the parent. Content that does not need to be updated by the user. 

What is the big difference between props and state?
Props passed into a component, and States are handled in side the component.
Props are outside and must be updated outside the component, States are inside and can be updated inside.
Use state when something needs to be updated by the user vs. props when you need it to be updated outside the component using a parent.

When do we re-render our application?
When you need to update your application after something the user has done.

What are some examples of things that we could store in state?
A counter, something that needs to be updated by the user.

# React Lifestyle
Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
The render happens first.

What is the very first thing to happen in the lifecycle of React?
Mounting is the first step.

Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

Constructor
Render
React Updates
componentDidMount
componentWillUnmount

What does componentDidMount do?
It's helpful in connecting APIs, and when you need to load something using a network request or intialize the DOM.
