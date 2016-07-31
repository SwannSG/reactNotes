#ReactJS#

##Introduction##

ReactJS implements HTML templating inside JavaScript.

The library is split into two broad modules *React* and *ReactDOM*.

ReactJS works with a shadow DOM to avoid frequent interaction with the real DOM. When actual DOM updates are to take place, React computes the difference between the shadow real DOM, and just applies the differences.

Acual DOM updates, which show up on the screen, use the *ReactDOM.render* method.

```JavaScript
var React = require('react');               // global React
var ReactDOM = require('react-dom');        // global ReactDOM

ReactDOM(<JSX expression>, <node inside real DOM>)  // place a number of nodes at a specific node
```

##JSX##

JSX is a DOM node describing language, that looks something like JavaScript and HTML, that can be used to generate nodes for the shadow DOM.

JSX understands elements eg. <p> and attributes <p someAttr='attribute'>.

JSX is converted to native JavaScript.

##JSX Expressions##
