# Lifecycle

![](/images/image_013.jpg)

Every React component is created, modified, and destroyed at some point. In the middle of these three steps, there are some phases that compose what we call the "lifecycle" of the component.

The lifecycle is nothing more than a set of phases by which a component passes from its creation to the moment it is destroyed. During each phase, you can perform specific actions to modify the state of the component.

## Phases of a React component

Components created with React passes through the following phases, throughout their lifecycle:

**1 - Mounting**

**2 - Updating**

**3 - Unmounting**

For each phase, React provides some "lifecycle methods" that you can override to perform actions whenever the component is in one of these phases.

### Mounting

The following methods are called when an instance of a component is being created and inserted into the DOM:

#### [constructor(props)](https://reactjs.org/docs/react-component.html#constructor)
> The constructor of a React component is called before it is assembled. When implementing the constructor for a React `Component` subclass, you must call `super(props)` before any other statement. Otherwise, `this.props` will be `undefined` in the constructor, which can lead to errors.


#### [static getDerivedStateFromProps(props, state)](https://reactjs.org/docs/react-component.html#static-getderivedstatefromprops)
> Is invoked right before calling the `render()` method, both on the initial mount and on subsequent updates. It should return an object to update the `state`, or `null` to update nothing.
>
> This method exists for rare use cases where the `state` depends on changes in `props` over time.


#### [render()](https://reactjs.org/docs/react-component.html#render)
> The `render()` function must be pure, which means that it does not modify the component's `state`, returns the same result each time it is invoked and does not interact directly with the browser. If you need to interact with the browser, run your operations on `componentDidMount()` or other lifecycle methods. Keeping pure rendering makes it easier to understand the components.
>
> The `render()` method is the only required method in a class component.


#### [componentDidMount()](https://reactjs.org/docs/react-component.html#componentdidmount)
> It is called immediately after a component is mounted. Initializations that require DOM nodes to exist must be called inside this function.
>
> If you need to load data from a remote endpoint, this is an excellent place to instantiate the network request.


### Updating

An update can be caused by changes in the `props` or `state`. These methods are called when a component is being **re-rendered**:


#### [static getDerivedStateFromProps(props, state)](https://reactjs.org/docs/react-component.html#static-getderivedstatefromprops)
> Is invoked right before calling the `render()` method, both on the initial mount and on subsequent updates. It should return an object to update the `state`, or `null` to update nothing.
>
> This method exists for rare use cases where the `state` depends on changes in `props` over time.


#### [shouldComponentUpdate(nextProps, nextState)](https://reactjs.org/docs/react-component.html#shouldcomponentupdate)
> Use this function to let React know if a component’s output is not affected by the current change in `state` or `props`.
>
> The default behavior is to re-render on every `state` change, and in the vast majority of cases you should rely on the default behavior.


#### [render()](https://reactjs.org/docs/react-component.html#render)
> The `render()` function must be pure, which means that it does not modify the component's `state`, returns the same result each time it is invoked and does not interact directly with the browser. If you need to interact with the browser, run your operations on `componentDidMount()` or other lifecycle methods. Keeping pure rendering makes it easier to understand the components.
>
> The `render()` method is the only required method in a class component.


#### [getSnapshotBeforeUpdate(prevProps, prevState)](https://reactjs.org/docs/react-component.html#getsnapshotbeforeupdate)
> `getSnapshotBeforeUpdate()` is invoked right before the most recently rendered output is committed to e.g. the DOM. It enables your component to capture some information from the DOM (e.g. scroll position) before it is potentially changed. Any value returned by this lifecycle will be passed as a parameter to `componentDidUpdate()`.


#### [componentDidUpdate(prevProps, prevState, snapshot)](https://reactjs.org/docs/react-component.html#componentdidupdate)
> Is invoked immediately after updating occurs. This method is not called for the initial render.
>
> Use this as an opportunity to operate on the DOM when the component has been updated.
>
> This is also a good place to do network requests as long as you compare the current props to previous props (e.g. a network request may not be necessary if the props have not changed).


### Unmounting

This method is called when a component is being removed from the DOM:


#### [componentWillUnmount()](https://reactjs.org/docs/react-component.html#componentwillunmount)
> Is invoked immediately before a component is unmounted and destroyed. Perform any necessary cleanup in this method, such as invalidating timers, canceling network requests, or cleaning up any subscriptions that were created in `componentDidMount()`.


## Lifecycle diagram

![](/images/image_014.jpeg)

**Is it still confusing?**

![](/images/image_015.gif)

Do not worry, in the Hands-on section we'll look at how a component's lifecycle works in practice 😉.
