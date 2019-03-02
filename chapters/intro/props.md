# Props

![](/images/image_008.png)

Every developer, regardless of language, framework or library, has at some point needed to pass parameters from one function to another.

In React we can also pass parameters from one component to another. We call this data `props`, an abbreviation for properties.

Let's look at a simple example:

```js
import React from 'react';

export default function Hello() {
  return (
    <span>Hello</span>
  );
};
```

This simple `hello.js` component displays the ***Hello*** message when another component calls it.

Imagine that now will be necessary to add a user name and this message dynamically.

We can refactor this component as follows:

```js
import React from 'react';

export default function Hello(props) {
  return (
    <span>Hello, { props.name }!</span>
  );
};
```

Now we can call this component inside another one, and pass the user name as a `prop`. In this case, the prop will be the `name` parameter:

```js
import React from 'react';
import Hello from './hello';

export default function App() {
  return (
    <div>
      <Hello name='Alice' />
    </div>
  );
};
```

The output for the above code will be:

![](/images/image_009.png)

The `props` are handy and make it possible to create flexible and even generic components.
