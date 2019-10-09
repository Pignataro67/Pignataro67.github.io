---
layout: post
title:      "A Brief Review of State/Updating State- React"
date:       2019-10-09 00:29:28 +0000
permalink:  a_brief_review_of_state_updating_state-_react
---

In a nut shell, State is a JavaScript Object that stores dynamic data in a React class component. State is initialized in the class constructor and is inserted into the component after super(props). There are many reasons to use state, two reasons are so you can create components that are both dynamic and interactive. Keys can be added to the component’s state with values. For example, a signup component can have a username and password state with keys and values as seen here:

class Signup extends Component { 
  constructor(props) { 
	  super(props); 
		  this.state = { 
		    username: '', 
		    password: '', 
    } 
  }

React provides a method called setState(), which is used to update or change the component’s initial state. An important rule to remember is that you can't update state directly with something like the following:

this.state.attribute = "new state"

The reason being is the above will not trigger a re-render of the component. Instead, you should create a new object that is passed into this.setState() with a key-value pair. This will cause the component to re-render with the new state. When the state updates, the component will re-render with the updated data.

Changing the state can be done with onClick events. When a user clicks on a button that has access to one of the built in functions, it will follow the actions that were created in the component. In this example there is a function called incrementCounter, which includes this.setState() to increment the counter by 1. 'Counter' is the state key while this.state.counter + 1 is the value.

incrementCounter = () => { 
  this.setState({ counter: this.state.counter + 1})
}

When I click a button that’s inside the return method of the render, it will re-render with the new data incremented to the next value and return it inside the h3 header. Since the button has access to 'incrementCounter' noted, you can use 'this.incrementCounter' and set it equal to onClick. This gives a user the ability to update data in real-time.

render() { 
  return ( 
    <div> <button onClick={this.incrementCounter}>Increment Counter</button> 
      <h3>{this.state.counter}</h3> 
    </div> 
  ) 
}

Since state changes can occur asynchronously, it's a good idea to implement a callback as the second argument in the setState() method in order to access the newly updated state. 

Another rule of state is that updates are merged on the first level. When "updating" one of the object keys, the other key-value pairs will remain the same. In order to update the key of another object inside the state, the spread operator(…) is used so the other keys and values of the previous object are not overwritten. 

Thanks for reading my post, I hope you enjoyed it.
