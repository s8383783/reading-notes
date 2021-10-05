# Putting it all together

What is the single responsibility principle and how does it apply to components?
Everything should have one job. Each component should have on responsibility.
What does it mean to build a ‘static’ version of your application?
a version that doesnt change.
Once you have a static application, what do you need to add?
state
What are the three questions you can ask to determine if something is state?
Is it passed in from a parent via props?
Does it remain unchanged over time? 
Can you compute it based on any other state or props in your component?

How can you identify where state needs to live
find every component that uses the state, or a common parent compoenet
What is a “higher-order function”?
a function that operates by taking other functions as a argument, or returning them
Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
is m is greater then n, return m
Explain how either map or reduce operates, with regards to higher-order functions.
The map method transforms an array by applying a function to all of its elements and building a new array from the returned values. The new array will have the same length as the input array, but its content will have been mapped to a new form by the function.
