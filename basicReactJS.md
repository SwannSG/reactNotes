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

JSX understands elements eg. `<p>` and attributes `<p someAttr='attribute'>`.

JSX is converted to native JavaScript.

##JSX Expressions##

May only have a single parent, which may or may not include children nodes.

Items inside curly brackets {....} belong to the JavaScript world.

```JavaScript
// examples of JSX expressions
<script type="text/babel">
    var jsWidth = 30;
    ReactDOM.render(
        (<img
            src="http://cdn.24.co.za/files/Cms/General/d/2991/10adb60279214215baf3bc15813a2ce3.png"
            alt="Nelson Mandela"
            class = "niceImg"
            any-attribute = 'any-value'
            width={jsWidth}                         // notice jsWidth is replaced by 30
        />),
        document.getElementById('id2')              // insert these node(s) at location 'id2'
      );
    </script>
```
Between the `<img` and end `/>` we have something similar to HTML. This is a JSX expression. Notice a multiline JSX expression is placed in parenthesis. We can place the contents on multiple lines for readability.
