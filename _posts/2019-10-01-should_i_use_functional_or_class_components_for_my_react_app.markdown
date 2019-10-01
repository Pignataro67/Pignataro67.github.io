---
layout: post
title:      "Should I use Functional or Class Components for my React App?"
date:       2019-10-01 14:36:11 +0000
permalink:  should_i_use_functional_or_class_components_for_my_react_app
---


React allows you to define functional components or class components. As the title implies you may be asking yourself how do I know when to use a functional component or class component? Below we will take a look at the differences between the two components.
Functional components are what their name implies. They are written as simple JavaScript functions and return a React element. They also use props which are arguments passed down to  them from the parent component. They are meant to be simple and concise:

function Greeting(props) { 
  return ( 
    <div> 
      <h1>Hola! {props.name}!</h1> 
    </div> 
	);
}

Class components are more complex because they allow us to have access to features like local state and lifecycle methods (i.e. componentDidUpdate and componentWillReceiveProps). In order to access these features, however, their syntax is a little different from functional components because they are a subclass of React.Component:

class Greeting extends React.Component { 
  render() { return (	 
	  <div>
		  <h1>Hola! {this.props.name}!</h1>	 
		</div>
		); 
	}
}

The line of code-- class and extends React.Component, is what gives this component access to additional features.
A good rule of thumb is to create your components as functional components, then change them to class components if the need arises within the component to add state or lifecycle methods. On the flip side you could create all the components as class components, because class components work in both situations, then refactor the ones that don’t need access to state or lifecycle methods into functional components later.  
Since functional components are easier to implement, I would recommend using them first. Then, depending on what each component does, you can easily create/change a functional component to a class component, if your component needs the additional features of a class component.
If you think about it from another perspective, all components could be class components and your app would work just fine, however, it would be more complex than it needs to be. Conversely, not all components can be functional components because they may need access to more features.
The cleanest approach is to plan ahead and determine what each component’s purpose is, for example, does it need state?  But if you can't, the next cleanest approach is to only do the extra work of creating a class component when the purpose of the component dictates it; You won't be doing any extra work and your components will reflect their intended purpose.
I hope you enjoyed my blog.
