# Virtual DOM

![](/images/image_001.jpg)

Without any doubt, one of React's most incredible things is [Virtual DOM](https://reactjs.org/docs/faq-internals.html#what-is-the-virtual-dom).

The v-dom it's an incredibly complex technique, that simulates in memory the [DOM](https://www.w3schools.com/whatis/whatis_htmldom.asp) structure. Through this in-memory representation, it is possible to manipulate the DOM in a fast and efficient way. What happens "behind the scene," is that any changes in your HTML structure is firstly made in the Virtual DOM and applied to the real DOM later.

When the Virtual-DOM object is updated, an algorithm calculates the difference between the v-dom and the real DOM, changing only the different chunks in the actual DOM. This type of technique is used to save the CPU and make the changes done optimally and quickly.

Experienced developers already know the pain and how slow is the manually DOM's manipulation.

The React efficiently solves this issue.

## Behaviour

Whenever the underlying data changes, the entire UI is rendered again in the Virtual DOM representation.

![](/images/image_002.png)

The difference between the previous DOM representation and the new one present in the v-dom is calculated.

![](/images/image_003.png)

Once the calculations are done, the actual DOM will be updated only with the things that have really changed.

![](/images/image_004.png)

Take in mind that this whole process is made incredibly fast, and you will see later in this tutorial the real benefits of this approach.
