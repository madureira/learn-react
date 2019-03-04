# Lifecycle

![](/images/image_013.png)

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

#### constructor(props)
> The constructor of a React component is called before it is assembled. When implementing the constructor for a React `Component` subclass, you must call `super(props)` before any other statement. Otherwise, `this.props` will be `undefined` in the constructor, which can lead to errors.

#### componentWillMount()
> It is invoked before the assembly occurs and is called before the `render()` function, so calling `setState()` synchronously in this method will not trigger an extra rendering. It is generally recommended to use the `constructor()`.
