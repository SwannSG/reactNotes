#ReactJS#

##Introduction##

ReactJS implements HTML templating inside JavaScript.

The library is split into two broad modules *React* and *ReactDOM*.

ReactJS works with a shadow DOM to avoid frequent interaction with the real DOM. When actual DOM updates are to take place, React computes the difference between the shadow DOM and real DOM, and just applies the differences.

Acual DOM updates, which show up on the screen, use the *ReactDOM.render* method.

```JavaScript
var React = require('react');               // global React
var ReactDOM = require('react-dom');        // global ReactDOM

ReactDOM(<JSX expression> or <JS node representation>, <node inside real DOM>)  // place a number of nodes at a specific node
```

##JSX##

JSX is a DOM node describing language, that looks something like JavaScript and HTML, that can be used to generate nodes for the shadow DOM.

JSX understands elements eg. <p> and attributes <p someAttr='attribute'>.

JSX is converted to native JavaScript.

##JSX Expressions##

May only have a single parent, which may or may not include children nodes.

Self-closing HTML tags must be closed with a closing tag.

Attribute `<p className="para">` converts to `<p class="para">`.

Items inside curly brackets {....} belong to the JavaScript world.

```JavaScript

// examples of JSX expressions
<p>Hello there</p>

var height = 10;
var width = 10;
(
    <img
        src = http://mysource.com/img1.jpg              // no quotes, no separating commas
        alt = River picture
        height = {height}                               // reference height in JS domain
        width = {width}
    </img>                                              // notice closing tag for image
)
```
