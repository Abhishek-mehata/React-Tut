


Expressions in JSX
-
```

-> By the help of curly baraces {} you can write expressions.
-> The expressions can be React Variable, or Propertt, or any Valid JS code.

Eg:
import React from "react";
import ReactDOM from "react-dom/client";

const myElement = <h1>React is {5 + 5} times better than JSX. </h1>

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```
--------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------

Some JSX rules in React:
--


Rule 1:
-
```
Inserting a Large Block of HTML
To insert Large block of HTML code you should use use parentheses '()' .

Eg:
['./src/main.jsx']

import React from "react";
import ReactDOM from "react-dom/client";

const myElement = (
    <ul>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
      <li>Apple</li>
    </ul>
)

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(myElement);
```

--------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------

Rule 2:
---
```
-> One Top Level Element
-> You should always wrap your HTML code inside one top level Element.
-> The top level Element is also called as Parent Element.

-> So, if you like to write two paragraphs, you must put them inside a parent element(like a <div> element) .

Eg:
['./src/main.jsx']

import React from "react";
import ReactDOM from "react-dom/client";

const myElement = (
  <div>
    <h1>I am a Header</h1>
    <h1>I am also a Header</h1>
  </div>
);
const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(myElement)

-> Note: JSX will throw an error if Our HTML is not wrapped inside a parent Element.

```
--------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------

Rule 3:
--
```
-> The Wrapper
-> You can  wrap multiple lines of HTML code using wrapper without adding any top level element.
-> This will prevent in case if you donot use parent element to your multi line HTML code.
-> This wrapper is also called 'fragment' 

-> A fragment looks like an empty tag: <></>

-> <!-- This will prevent unnecessarily adding extra nodes to DOM. -->

Eg:
['./src/main.jsx']

import React from "react";
import ReactDOM from "react-dom/client";

const myElement = (
  <>
    <p>I am a para</p>
    <p>I am also a para</p>
  </>
);

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(myElement);
```
--------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------


Rule 4:
--
```
-> Elements Must be Closed
-> Since JSX follows XML rules, every HTML elemnts must be properly closed.Weather the tags are paired tags or unpaired tags.

Eg:
['./src/main.jsx']

import React from "react";
import ReactDOM from "react-dom/client";

const myElement=(
  <>
    <label>Name: </label>
    <input type="text" placeholder="Enter your Name Here" />
  </>
);

const root=ReactDOM.createRoot(document.getElementById("root"));
root.render(myElement);

-> Note: JSX will throw an error if the HTML is not properly closed.
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Rule 5:
---
```
Attribute 'class' = 'className'

-> The 'class' attribute is used inside HTML tags.
-> Since 'class' is reserved keyword in JS and JSX is rendered as JS in runtime. 
-> 'className' attribute is used in JSX  instead of 'class' attribute.

-> Note: In JSX (used in React), instead of using class to add styles like in regular HTML, you have to use className. JSX then automatically changes className back to class so the browser can understand it. So, className in JSX works the same as class in HTML; it’s just a naming rule in React.


Eg:

<!-- ./src/main.jsx -->

import React from 'react';
import ReactDOM from 'react-dom/client';

const myElement = <h1 className='myClass'>Hello World</h1>

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);

____________________________________________________________________________

<!-- ./index.html -->
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite + React</title>
    <style>
      .myClass{
        color: red;
      }
    </style>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```

---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------

Rule 6:
---

```
-> Conditions - if statements

-> React allows you to use if statements, but not directly inside the JSX code (JSX-the part that looks like HTML).

-> To use conditions in JSX :

                            1] You should write 'if' statement outside the JSX and then use the result inside JSX.
                            2] You can use ternary operator as an inline approach.
______________________________________________________________

Eg1:
<!-- Write if statements outside of the JSX code -->

import React from 'react';
import ReactDOM from 'react-dom/client';

const x = 5;
let text = "Goodbye";
if (x < 10) {
  text = "Hello";
}

const myElement = <h1>{text}</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);


__________________________________________________________________________

Eg2:
<!-- Use ternary expressions instead -->
import React from 'react';
import ReactDOM from 'react-dom/client';

const x = 5;

const myElement = <h1>{(x) < 10 ? "Hello" : "Goodbye"}</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);


-> Note: To use JS expression/code inside JSX, it must be wrapped inside curly braces, {} 
```
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
