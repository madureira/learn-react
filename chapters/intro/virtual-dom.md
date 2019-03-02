# Virtual-DOM

Without a doubt, one of React's most incredible things is Virtual-DOM.

The v-dom it's an incredibly complex technique, that simulates in memory the DOM structure. Through this in-memory representation, it is possible to manipulate the DOM in a fast and efficient way. What happens "behind the scene," is that any changes in your HTML structure is firstly made in the virtual-DOM and applied to the real DOM later.

When the Virtual-DOM object is updated, an algorithm calculates the difference between the v-dom and the real DOM, changing only the different chunks in the actual DOM. This type of technique is used to save the CPU and make the changes done optimally and quickly.

Experienced developers already know the pain and how slow is the manually DOM's manipulation.

The React efficiently solves this issue.

## Behaviour

Whenever the underlying data changes, the entire UI is rendered again in the Virtual-DOM representation.

![](/images/image_1.png)
