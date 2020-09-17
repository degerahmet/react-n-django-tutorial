# React and Django Tutorial
This repository was created to improve my front-end skills and combine them with my back-end skills.

## Why React ? 

### Imperative Programming 

View:
```html
<h1> 0 </h1>
```
Logic:
```javascript
let num = parseInt(document.querySelector("h1").innerHTML);
num += 1;
document.querySelector("h1").innerHTML = num;
```

React allows us to use declarative programming, which will allow us to simply write code explaining what we wish to display and not worry about how we’re displaying it. In React, a counter might look a bit more like this:

### Declarative Programming
```html
<h1>{num}</h1>
```
Logic:
```javascript
num += 1;
```

The **React** framework is built around the idea of components, each of which can have an underlying state. A component would be something you can see on a web page like a post or a navigation bar, and a state is a set of variables associated with that component. The beauty of React is that when the state changes, React will automatically change the DOM accordingly.

* `React`   : Defines components and their behavior
* `ReactDOM`: Takes React components and inserts them into the DOM
* `Babel`   : Translates from JSX, the language in which we’ll write in React, to plain JavaScript that our browsers can interpret. JSX is very similar to JavaScript, but with some additional features, including the ability to represent HTML inside of our code.

How to looks like HTML page with React : 
```html,javascript
<!DOCTYPE html>
<html lang="en">
    <head>
        <script src="https://unpkg.com/react@16/umd/react.development.js" crossorigin></script>
        <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js" crossorigin></script>
        <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
        <title>Hello</title>
    </head>
    <body>
        <div id="app" />
        <script type="text/babel">

            class App extends React.Component {

                render() { 
                    return (
                        <div>
                            <h1>Welcome!</h1>
                            Hello!
                        </div>
                    );
                }
            }
             
            ReactDOM.render(<App />, document.querySelector("#app"));
        </script>
    </body>
</html>
```

* In the three lines above the title, we import the latest versions of React, ReactDom, and Babel.
* In the body, we include a single `div` with an `id` of `app`. We almost always want to leave this empty, and fill it in our react code below.
* We include a script tag where we specify that `type="text/babel"`. This signals to the browser that the following script needs to be translated using Babel.
* Next, we create a component called `App` that extends `React.Component`. Components in React are represented as JavaScript classes, which are similar to the Python classes we learned about earlier. This allows us to start creating a component without rewriting a lot of code included in the `React.Component` class definition.
* Inside of our component, we include a render function. All componenets are required to have this function, and whatever is returned within the function will be added to the DOM, in this case, we are simply adding `<div>Hello!</div>`.
* The last line of our script employs the `ReactDOM.render` function, which takes two arguments:
  * A component to render
  * An element in the DOM inside of which the component should be rendered
Now that we understant what the code is doing, we can take a look at the resulting webpage:
