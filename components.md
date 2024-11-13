Componensts are like functions that returns HTML Elements.
---


React Components:
---
```
-> Components are independent and reusable bits of code.
-> They’re like JavaScript functions but are designed to work independently and generate HTML code.
```
---
---

Types of Components
----
```
There are two main types of components:
1] Class Components
2} Function Components
In this tutorial we will concentrate on Function components.


-> Note:In older React code bases, you may find Class components primarily used. It is now suggested to use Function components along with Hooks, which were added in React 16.8. There is an optional section on Class components for your reference.
```

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Create Your First Component
---

# When creating a React component, the component's name MUST start with an upper case letter.


Class Component:
---

```
A Class Component in React needs to include the line `extends React.Component`. This connects your component to React.Component, giving it access to React's built-in functions.

Class components also need a `render()` method.



Eg:
# './src/components/welcome.jsx'

import React from 'react';

class Welcome extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, Welcome to React!</h1>
      </div>
    );
  }
}

export default Welcome;

# // 1] class Welcome extends React.Component: This creates a class called Welcome that "inherits" from React.Component, making it a React component

# // 2] render() method: Inside the class, we define a render() method. This method must be there for a class component, and it tells React what HTML to display/render.

# // 3] Returning HTML: Inside render(), we return the HTML that will be shown, which here is a div with a heading that says "Hello, Welcome to React!".


-----------------------------------_____________________________________________________

# './src/App.jsx'
import Welcome from "./components/welcome.jsx";

function App(){
  return(
    <div>
      <Welcome/>
    </div>
  )
}


export default App;
```
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Function Component
---
```

# A Function component also returns HTML, and behaves much the same way as a Class component, but Function components can be written using much less code, are easier to understand, and will be preferred in this tutorial.


Eg:

# './src/comonents/car.jsx'

function car(){
    return(
        <>
            <p>This is a car component.</p>
        </>
    )
}

export default car;

-----------------------------------------------------------

# './src/App.jsx'
import Car from "./components/Car";

function App() {
  return(
    <Car/>
  )
}

export default App
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


