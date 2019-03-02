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
import React from 'react';

class Like extends React.Component {

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
