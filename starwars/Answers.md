# Answers

1. What is React JS and what problems does it try and solve? Support your answer with concepts introduced in class and from your personal research on the web.

React JS is a JavaScript library for building composable user interfaces with reusable components that react to data changes. It is maintained by Facebook and a community of individual developers and companies. Often problems solved by React are for instance while working with templates or HTML directives, React components call a render method that produces a string of markup, then injects this directly into your document. Whenever the data changes, React calls a new render method. Also, renders the right components  by handling instantly better dynamic data for faster response times and a smooth user experience.

1. What does it mean to think in react?

Recat thinks chiefly in two phases: The render phase determines what changes need to be made to e.g. the DOM. During this phase, React calls render and then compares the result to the previous render. The commit phase is when React applies any changes. (In the case of React DOM, this is when React inserts, updates, and removes DOM nodes.) 

Consequently, this is what it means to think with React: install dependencies on your laptop, open your editor and build a component hierarchy. Next, build a version that takes your data model and renders the UI, build components that reuse other components and pass data using props, start with building the components higher up in the hierarchy (top-down approach), keep testing by console logging, identify the minimal representation Of UI State thru Hooks to make your UI interactive, so you would be able to trigger changes to your underlying data model, at this point to build your app correctly, you first need to think of the minimal set of mutable state that your app needs. The key here is DRY: Don’t Repeat Yourself, identify which component mutates, or owns, this state, Identify every component that renders something based on that state, If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component, make sure that whenever the user changes the form, we update the state to reflect the user input, pass callbacks to update the app, be patient, debugs and console.log often and Eureka sync your terminal to ensure localhost display properly.

1. Describe state.

A React JS anchor concept to declare multiple variables,  fully controlled by composed components in order to render and re-rendar upon functions (i.e. Effect Hooks, etc). 

1. Describe props.

 Props is a function that a component uses to know what to render.

1. What are side effects, and how do you sync effects in a React component to state or prop changes?

A "side effect" is anything that affects something outside the scope of the function being rendered. you sync effect in a component to calling setState() in componentWillReceiveProps doesn't cause additional re-render. Receiving props is one render and this.setState would be another render if that were executed within a method like componentDidUpdate. 