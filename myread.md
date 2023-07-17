`ReactDOM.render()`

This method comes from `react-dom` package, and takes two arguments;

- A **React component** to render (typically, we'll render our top-level `App` component here).

- A **DOM element** where we want that component to be rendered (by convention, a `div` with the ID of `root`) this is in html.


`App.js`

This is all js.

 The HTML-like syntax is
called JSX. It lets us write code that looks nearly identical to HTML, but
allows us to mix in vanilla JavaScript and other neat things.

**example**

import React from "react";
import { format } from "date-fns";
import ExampleComponent from "./ExampleComponent";

// Add your code own within the return statement
function App() {
  return (
    <div className="App">
      <h1>{format(new Date(), "MMMM do yyyy, h:mm:ss a")}</h1>
      <p className="App-intro">
        In React apps, we write JSX - it looks like HTML, and uses a lot of HTML
        syntax. JSX lets us include JavaScript functions right along with the
        HTML, and also allows us to add in components, which are separate,
        self-contained chunks of JSX.
      </p>
      <ExampleComponent />
    </div>
  );
}

export default App;

`App` is at the top-most level; it is the parent component of our React app content, but we can add the children here though a repetition


## Importing, Exporting, and the Dependency Tree

Here we have import and export.

```js
import React from "react";
import { format } from "date-fns";
import ExampleComponent from "./ExampleComponent";

function App() {
  // etc
}

export default App;
```
App.js is pulling two specific content from packages react and date-fns.

(react and date-fns)are being _imported_ from the `node_modules` folder, which was
created when we ran `npm install`.


 By importing `./ExampleComponent`, we make `<ExampleComponent />`
available for use in the `App` component's return statement.

`in index.js`

import React from "react";
import ReactDOM from "react-dom";
import App from "./components/App";
import "./index.css";

ReactDOM.render(<App />, document.getElementById("root"));

i'll be using import for files that have being exported.


# Debugging Components

Here we use the extenstion React Developer Tools.

find the Components tab. Here, you'll see the component hierarchy with information about all the components we're using so far in the app!.


