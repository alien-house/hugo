---
title: "React 7 Tips for beginners on Getting Started"
description : "This is for"
date: 2017-12-04T13:12:55-08:00
draft: false
slug: "react_guide_for_beginners"
tags: ["react", "javascript"]
---

Now 2017, although It has been for over 4 years from the Initial release of React, I haven't introduced it to my projects yet😓  I want to learn so that I dive into React and implemented some projects. In order to get used to the one of a front-end technology.
I found out something necessary topics during the creating some Apps. Here are the most important 7 concepts when you create React Web App.

## Table of Contents
1. [What is React?](#what-is-react)
	- [How can you start to create React App?](#how-can-you-start-to-create-react-app)
1. [What makes React so fast?](#what-makes-react-so-fast)
1. [What is the lifecycle of a React component?](#what-is-the-lifecycle-of-a-react-component)
1. [What is JSX?](#what-is-jsx)
1. [What are State and Props?](#what-are-state-and-props)
1. [What is refs?](#what-is-refs)
1. [What is pros and cons of React?](#what-is-pros-and-cons-of-react)

## What is React?
 
> "A JavaScript library for building user interfaces."  
"React is an open-source JavaScript library for building user interfaces created by Facebook in web and mobile applications."

One of the benefits of the React is to make developing a large scale single page application easier.
Another feature of React is the virtual DOM. whenever a change happens, the virtual DOM efficiently re-renders the DOM.

### How can you start to create React App?
When you want to start create an actual project, then you can use ["create-react-app"](https://reactjs.org/docs/installation.html#creating-a-new-application).
```
npm install -g create-react-app
create-react-app my-app

cd my-app
npm start
```

It's so simple! You don't need to worry about any dependencies like Babel and webpack. it will be automatically installed.

#### Requiement
- Node >= 6
- npm 5.2.0+

*If you want to use as a part of project. you need to install by yourself.  
[Adding React to an Existing Application](https://reactjs.org/docs/installation.html#adding-react-to-an-existing-application)

## What makes React so fast? 
React has a virtual DOM that writes to the browser DOM only when it needs to.
When we call the render function, React will update the virtual DOM. That will push only the necessary changes to the real DOM.

> 1. Whenever anything may have changed, the entire UI will be re-rendered in a Virtual DOM representation.
> 2. The difference between the previous Virtual DOM representation and the new one will be calculated.
> 3. The real DOM will be updated with what has actually changed. This is very much like applying a patch.


## What is the lifecycle of a React component?
When render() method is called when is state or props has changed, fall into following step:

> React components have lifecycle events that fall into three general categories:
> 
> 1. Initialization ex.componentwillmount()
> 2. State/Property Updates
> 3. Destruction

and here are more in detail:

### Mounting
Mounting flow is just called once when a component is created.

1. constructor()
2. componentDidMount()
3. componentWillUnmount()
4. render()

### Updating
When states or props change, the flow is going to be executed.

1. componentWillReceiveProps()
2. shouldComponentUpdate()
3. componentWillUpdate()
4. render()
5. componentDidUpdate()

What I want to show here is you can filter whether a specific states or props change or not, in order to reduce rendering.



## What is JSX?
>
It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

As React maker recommend that, it is not requirement. However, if you use JSX, you can write simpler. because its like a HTML syntax. React provides virtual DOM that you can create them using "React.createElement".   
Here are the compare to creating DOM using JSX and React.createElement:

**JSX:**

	const App = (props) => {
		return (
			<div>
				<a></a>
			</div>
		)
	}

**React.createElement:**

	var App = function App(props) {
		return React.createElement(
			"div", 
			null,
			React.createElement("a", null)
		);
	}




## What are State and Props?
State is mutable data. and maintained by component. it can be changed but should be considered as private.

Props (properties) are values which are passed into a component from its parent. Props are immutable data. it can't be changed.


## What is refs?
When we want to check or find the specific components, if you use refs, you can get and manipulate it.

> There are a few good use cases for refs:
> 
- Managing focus, text selection, or media playback.
- Triggering imperative animations.
- Integrating with third-party DOM libraries.

https://reactjs.org/docs/refs-and-the-dom.html

Also, if the child comment which has method, its can be called the method from parent component.


## What is pros and cons of React?
### Pros
- If you are familiar with Javascript based project, Learning Curve is relatively low.
- It can be used Javascript(ES6).
- site performance is good in terms of using Virtual DOM.
- JSX you are supposed to use is looks similar to HTML.
- React is library, so that you can combine any other liberies.

### Cons
- If you have never created project Javascript main, you need to  learn ES6 and class-based concepts first. 
- It's so simple that is often needed other libraries such as React-router or Redux.
- It might be complex and messy because it is going to be so many components as the project became bigger.



## Conclusion
Through the React App creating, it's easier to create than using pure Javascript from scratch. There is still a lot of things I need to learn more such as getting used to ES6, Redux (and concepts of Flux), creating React library, comparing other framework and libraries. I'm gonna post after research these things.


## General Reference and Related articles
- [DOCS : React.Component](https://reactjs.org/docs/react-component.html)
- [5 Essential React.js Interview Questions and Answers](https://www.codementor.io/blog/5-essential-reactjs-interview-questions-du1084ym1)
- [Everything You Should Know About React: The Basics You Need to Start Building](https://medium.freecodecamp.org/everything-you-need-to-know-about-react-eaedf53238c4)












