<h1>Life Cycle</h1>
<p>n React, components have a lifecycle that consists of different phases. Each phase has a set of lifecycle methods that are called at specific points in the component's lifecycle. These methods allow you to control the component's behavior and perform specific actions at different stages of its lifecycle.A component's lifecycle has three main phases: the Mounting Phase, the Updating Phase, and the Unmounting Phase.The Mounting Phase begins when a component is first created and inserted into the DOM. The Updating Phase occurs when a component's state or props change. And the Unmounting Phase occurs when a component is removed from the DOM.</p>
<h3>Component Mounting Phase</h3>
<p>The mounting phase refers to the period when a component is being created and inserted into the DOM.During this phase, several lifecycle methods are invoked by React to enable the developer to configure the component, set up any necessary state or event listeners, and perform other initialization tasks.</p>
<h4>The constructor() lifecycle method</h4>
<p>The constructor() method is called when the component is first created. You use it to initialize the component's state and bind methods to the component's instance.</p>

<h4>The render() lifecycle method</h4>
<p>The render() method is responsible for generating the component's virtual DOM representation based on its current props and state. It is called every time the component needs to be re-rendered, either because its props or state have changed, or because a parent component has been re-rendered.</p>

<h4>The getDerivedStateFromProps() lifecycle method</h4>
<p>During the mounting phase, getDerivedStateFromProps() is called after the constructor and before render(). This method is called for every render cycle and provides an opportunity to update the component's state based on changes in props before the initial render.</p>

<h4>The componentDidMount() lifecycle method</h4>
<p>The componentDidMount() method is called once the component has been mounted into the DOM. It is typically used to set up any necessary event listeners or timers, perform any necessary API calls or data fetching, and perform other initialization tasks that require access to the browser's DOM API.</p>

<h3>Component Updating Phase</h3>
<h4>The shouldComponentUpdate() lifecycle method</h4>
<p>The shouldComponentUpdate()  method is called before a component is updated. It takes two arguments: nextProps and nextState. This method returns a boolean value that determines whether the component should update or not. If this method returns true, the component will update, and if it returns false, the component will not update.</p>

<h4>The componentWillUpdate() lifecycle method</h4>
<p>omponentWillUpdate() is a lifecycle method in React that gets called just before a component's update cycle starts. It receives the next prop and state as arguments and allows you to perform any necessary actions before the component updates. But this method is not recommended for updating the state, as it can cause an infinite loop of rendering. It is primarily used for tasks such as making API calls, updating the DOM, or preparing the component to receive new data. componentWillUpdate() is often used in conjunction with componentDidUpdate() to handle component updates.</p>

<h4>The componentDidUpdate lifecycle method</h4>
<p>The componentDidUpdate() method is a lifecycle method in React that is called after a component has been updated and re-rendered. It is useful for performing side effects or additional operations when the component's props or state have changed.</p>

<h4>The getSnapshotBeforeUpdate lifecycle method</h4>
<p>The getSnapshotBeforeUpdate() method is called just before the component's UI is updated. It allows the component to capture some information about the current state of the UI, such as the scroll position before it changes.</p>

<h3>Component Unmounting Phase</h3>
<p>The unmounting phase refers to the lifecycle stage when a component is being removed from the DOM (Document Object Model) and is no longer rendered or accessible.

During this phase, React performs a series of cleanup operations to ensure that the component and its associated resources are properly disposed of.

The unmounting phase is the last stage in the lifecycle of a React component and occurs when the component is being removed from the DOM tree.

This can happen for various reasons, such as when the component is no longer needed, the parent component is re-rendered without including the child component, or when the application is navigating to a different page or view.</p>

<h4>The componentWillUnmount() lifecycle method</h4>
<p>componentWillUnmount(): This method is called just before the component is removed from the DOM. It allows you to perform any necessary cleanup, such as canceling timers, removing event listeners, or clearing any data structures that were set up during the mounting phase.
After componentWillUnmount() is called, the component is removed from the DOM and all of its state and props are destroyed.</p>

<hr/>

<h1> Props And State</h1>
<h3>State</h3>
<p>The state is an updatable structure that is used to contain data or information about the component and can change over time. The change in state can happen as a response to user action or system event. It is the heart of the react component which determines the behavior of the component and how it will render. A state must be kept as simple as possible. It represents the component's local state or information. It can only be accessed or modified inside the component or by the component directly.</p>

<h3>Props</h3>
<p>Props are read-only components. It is an object which stores the value of attributes of a tag and work similar to the HTML attributes. It allows passing data from one component to other components. It is similar to function arguments and can be passed to the component the same way as arguments passed in a function. Props are immutable so we cannot modify the props from inside the component.</p>

<hr/>

<h1>Functional And Class Components</h1>
<h3>Functional Components</h3>
<p>A functional component is just a plain JavaScript pure function that accepts props as an argument and returns a React element(JSX).There is no render method used in functional components.Functional components run from top to bottom and once the function is returned it can’t be kept alive.Also known as Stateless components as they simply accept data and display them in some form, they are mainly responsible for rendering UI.React lifecycle methods (for example, componentDidMount) cannot be used in functional components.Hooks can be easily used in functional components to make them Stateful.Constructors are not used.</p>

<h3>Class Components</h3>
<p>A class component requires you to extend from React. Component and create a render function that returns a React element.It must have the render() method returning JSX (which is syntactically similar to HTML).The class component is instantiated and different life cycle method is kept alive and is run and invoked depending on the phase of the class component.Also known as Stateful components because they implement logic and state.React lifecycle methods can be used inside class components (for example, componentDidMount).It requires different syntax inside a class component to implement hooks.It requires different syntax inside a class component to implement hooks.</p>

<hr/>

<h1>Virtual DOM</h1>
<p>The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library such as ReactDOM. This process is called reconciliation.Virtual DOM makes the performance faster, not because the processing itself is done in less time. The reason is the amount of changed information – rather than wasting time on updating the entire page, you can dissect it into small elements and interactions</p>

<hr/>













