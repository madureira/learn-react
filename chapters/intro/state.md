# State

![](/images/image_010.png)

State can be defined as: The place from which the information of a component comes and transforms throughout its life cycle.

The state stores the values of a Component and only it can change the state itself.

The state of a Component can be created from props, but cannot be inherited from the parent Component.

**The State should be considered as private data.**

Still, do not understand what the State is or how it works?

Let's look at some practical examples.

Imagine that you need to create a component to display the number of Likes in a post.

Initially, we could create something like:

```js
import React, { Component } from 'react';

class Like extends Component {

  render() {
    return (
      <div>
        <p>This is my article. Did you like it?</p>
        <button>Like</button>
        <span>0</span>
      </div>
    );
  }

}

export default Like;
```

![](/images/image_011.png)


Now we need to add an event on the button to let the counter know that the number of Likes has changed.

That's where the state comes into play!

Through the state, we will have an initial value for this counter, that is **0** (zero), as the user clicks the like button, the number will be incremented.

Let's add an initial state for this component:

```js
import React, { Component } from 'react';

class Like extends Component {

  constructor(props) {
    super(props);
    this.state = {
      likes: 0
    };
  }

  render() {
    return (
      <div>
        <p>This is my article. Did you like it?</p>
        <button>Like</button>
        <span>{ this.state.likes }</span>
      </div>
    );
  }

}

export default Like;
```
