# React Questions.

## 1. What are the differences between functional and class components?

Before the introduction of Hooks in React, functional components were called stateless components and were behind class components on feature basis. After the introduction of Hooks, functional components are equivalent to class components.

Although functional components are the new trend, the react team insists on keeping class components in React. Therefore, it is important to know how these both components differ.

Key points:

- Class components have various lifecycle methods, whereas functional has `useEffect` which is a combination of `componentDidMount` and `componentDidUpdate`.
- Syntax of class components is more complex than functional components.
- Hoisting works only for functional components.
- Less code means it can be more readable.


**Notes:**  
So the key take away is they should understand that they are both valid ways of writing components, but functional are more common in the new version of React and they do have slightly better performance and a better developer flow, example using `const [count, setCount] = React.useState(0);` which is faster to write and it offers the set method for you instead.

---


## 2. What is the difference between props and state?

Props are the data that is passed to the component. State is the data that is stored in the component.

**Notes:**  
Knowing the key destinction here is that props are imutable and state is mutable.

---

## 3. Explain the difference between PureComponent and Component.

The main difference here is that a PureComponent will do a shallow comparison against it's props and state to see whether it should re-render, essentially implenting a `shouldComponentUpdate` method. There is a caveat which is that it is a shallow comparison, meaning it will only pay attention to the top object level of the state.

**Note:**  
Would be good for the candidate to explain the noted caveat.

---

## 4. What is the difference between `React.Fragment` and `React.Children`?

React.Children is a utility function that allows you to pass a list of children to a component. React.Fragment is a component that renders its children.

**Note:**  
Basic level knowledge, but good to hear.

---

## 5. What are synthetic events in React?

Synthetic events combine the response of different browser's native events into one API, ensuring that the events are consistent across different browsers. The application is consistent regardless of the browser it is running in. Here, preventDefault is a synthetic event.

**Note:**  
It would be good to hear that the candidate understands that it's an event wrapper essentially that aims to be consistent across all browsers.

---

## 6. How do you give the right context to a method when using class component syntax?

So a class component is a standard class that extends the `React.Component` or `React.PureComponent` class, now the big part here is that when we create a method inside of the class like `handleClick()`, we need to make sure the component has the right context, otherwise the component will not be able to use the method.

To do this you can do one of two ways:

```javascript
class MyComponent extends React.Component {
	constructor() {

		// Binds to the component's context.
		this.handleClick = this.handleClick.bind(this);
	}

	handleClick() {
		// Do something
	}

	render() {
		return (
			<button onClick={this.handleClick}>Click Here!</button>
		);
	}
}
```

Or you can do:

```javascript
class MyComponent extends React.Component {
	handleClick() {
		// Do something
	}

	render() {
		return (
			<button onClick={(e) => this.handleClick(e)}>Click Here!</button>
		);
	}
}
```

Again note that we wrap the `handleClick` method in a function that takes in the event object as an argument and by doing this it will be a function called in the component context therefore using the right context when calling the method.

**Note:**  
Here we just want to know that the candidate is aware of this and they know the two methods to do so.

---

## 7. When using the setState method, why would you pass a function instead of an object?

So here we are talking about doing: `this.setState((prevState) => {});` instead of `this.setState({});` the reason for doing so is that the setState method is asynchronous and therefore we need to pass a function that will be called when the state is updated with the previous state as the argument. So if you have a counter than on click will increment the counter, then you would do:

```javascript
this.setState((prevState) => {
	return {
		count: prevState.count + 1
	};
});
```

Instead of:

```javascript
this.setState({
	count: this.state.count + 1
});
```

If you did the last one, then bugs could be introduced where the state may change while the state is being updated and therefore producing undiserable results.

**Note:**  
Here we want to make sure the user is aware of this and they know the difference between the two.