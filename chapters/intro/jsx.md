# JSX

![](/images/image_005.png)

Let's consider the follow variable declaration:

```js
const element = <h1>Hello World!</h1>;
```

This Tag syntax is not a string or even an HTML.

This kind of statement is called **J**avaScript **S**yntax e**X**tension, or simply [**JSX**](https://reactjs.org/docs/introducing-jsx.html), and is nothing more than a syntax extension of JavaScript.

At first glance, many people "wring their nose" at JSX because we're merging HTML with JavaScript.

However, this decision is sage as we have been able to create self-supporting components, i.e., components written using JSX have everything they need to work stand-alone.

Rather than artificially separating technologies by placing markup and logic in separate files, React separates concerns with slightly-coupled drives, called "components" that contain both.

## Embedding expressions in JSX

Because JSX is a JavaScript extension, you can incorporate any expression by wrapping it in braces `{}`.

Let's look at the example below:

```js
function getName() {
  return 'Alice';
}

const element = (
  <h1>Hello, { getName() }</h1>
);
```

After compilation, JSX expressions become regular JavaScript function calls.

Below we have the resulted code from the JSX above:

```js
'use strict';

function getName() {
  return 'Alice';
}

var element = React.createElement(
  'h1',
  null,
  'Hello, ',
  getName()
);
```

## JSX is also an expression

As we saw above, after compiling the JSX becomes standard Javascript code, so we can use JSX inside `if` statements and `for` loops, assign it to variables, accept it as arguments and return functions:

```js
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {user.name}</h1>;
  } else {
    return <h1>Hello, Stranger.</h1>;
  }
}

const element = (
  <div>
    { getGreeting({ name: 'Alice' }) }
  </div>
);
```

## Specifying attributes with JSX

You can declare attributes in JSX as you usually do in HTML. However, it's important to note that since JSX closer to Javascript than HTML, the syntax for JSX attributes uses the [CamelCase](https://en.wikipedia.org/wiki/Camel_case) property naming convention instead of HTML attribute names.

For example, the HTML attribute `class` becomes `className` in JSX, and `tabindex` becomes `tabIndex`.

Here are some examples:

```js
const element = <div className='modal'></div>;
```

```js
const element = <div tabIndex='0'></div>;
```

```js
const element = <input type='text' readOnly={true} />
```

## Specifying children with JSX

If a tag is empty, you can close it immediately with `/>`, as we do in [XML](https://www.w3schools.com/xml/xml_whatis.asp):

```js
const element = <div className='background' />;
```

JSX tags may contain children:

```js
const element = (
  <div>
    <h1>Hello!</h1>
  </div>
);
```
