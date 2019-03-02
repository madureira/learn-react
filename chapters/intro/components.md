# Components

![](/images/image_006.png)

As stated earlier, React helps us create UI and for that, allows you to create components by increasing code reuse, productivity, and organization of your project.

Let's take a look at the anatomy of a React component:

```js
import React from 'react';

export default function Button() {
  return (
    <button onClick={ function() { alert('Clicked'); } }>
      Click me
    </button>
  );
};
```

As you may have noticed, a React component is nothing more than a `function`.

What the above code does is generate a component called **Button**, which has a simple HTML structure containing the `<button>` tag and also a click event associated with that tag.

In addition to `functions`, we can also represent React components through *classes*.

```js
import React from 'react';

export default class Button extends React.Component {
  render() {
    return (
      <button onClick={ function() { alert('Clicked'); } }>
        Click me
      </button>
    );
  }
};
```

Later we will see the difference between these two approaches and when you should choose one instead of the other.

To make use of this component, we could call it through another component:

```js
import React from 'react';
import Button from './button';

export default function App() {
  return (
    <div id='app'>
      <Button/>
    </div>
  );
};
```

Notice how we insert our `<Button/>` component into another component, in this case, the `App` component.

The output for the above code will be:

![](/images/image_007.png)
