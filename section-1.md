## Prerequisites

###

### What is JSX?
JSX stands for Javascript XML. JSX is a syntax extension of Javascript that allows us to wrtie HTML in React. It allows for us to create HTML elements in Javascript and place them in the DOM without using any createElement() and/or appendChild methods()


#### JSX example

```
import React from 'react'

function Greet(){
  return <h1>Hello World!</h1>
}
```
Because JSX is not able to be read by browsers, we need a transpiler to translate it to React.createElement() calls. So the following code above is transpiled to the following:
```
import React from 'react'

function Greet() {
  return React.createElement("h1", {}, "Hello, World!")
}
```


### What are components
React Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML. Components can come in two types: class components or functional components.
#### Class Component
```
class HelloWorldApp extends React.Component {
  render() {
    return <h2>Hello World</h2>;
  }
}
```
#### Functional component
```
function HelloWorldAppp() {
  return <h2>Hello World</h2>;
}
```

### Props
Props are an important concept to understand in both React and React Native. Most components can be customized when they are created with different parameters. These parameters are called props and you can use props to pass data and values from one component to another. How props are passed into a component is similar to how attributes work in HTML elements. Props are variables that we pass from a parent component to a chuld component.
Passing props into components looks like this:
``` 
<ComponentName property1="value" property2="value" property3="value" /> 
```
Example of using props in a component
```
function Product(props) {
    return (
      <div>
        <img src={props.objectName} alt="products" />
        <h4>{props.objectName}</h4>
        <p>{props.objectName}</p>
        <h4>{props.objectName}</h4>
      </div>
    );
}

export default Product
```

### State
While props are read-only and cannot be modified, state allows react components to initialize and manage variables internally. There is no different between handling state in React and React Native. To manage state, you begin by importing useState from react.

```
import {useState} from 'react';

const App = () => {
      const [count, setCount] = useState(0);

  return (
    <View style={styles.container}>
      <Text>You clicked {count} times</Text>
      <Button
        onPress={() => setCount(count + 1)}
        title="Click me!"
      />
    </View>
  );
};
}
```


### Resources:
- [React Native Basics](https://reactnative.dev/docs/tutorial)
- [Introducing JSX](https://legacy.reactjs.org/docs/introducing-jsx.html)
- [How JSX works under the hood](https://www.telerik.com/blogs/how-jsx-react-works-under-hood)
- [React.Component](https://legacy.reactjs.org/docs/react-component.html)
- [React components](https://www.w3schools.com/react/react_components.asp)
- [React Props](https://www.freecodecamp.org/news/how-to-use-props-in-reactjs/)