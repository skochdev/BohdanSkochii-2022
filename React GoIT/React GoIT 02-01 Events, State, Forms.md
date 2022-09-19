- Class method **render()** should return only the markup, and nothing more than that.

- React has event delegation  pre-arranged by default for you. No need to worry about it.

## How to re-write state value

```js
export class Counter extends Component {  
  state = {  
    value: 0,  
  };  
  
  handleIncrement = () => {  
    this.setState({  
      value: 101,  
    });  
  };
}
```

- State update is async

## How to update state  based on the current value

```js
handleIncrement = () => {  
  this.setState(prevState => ({ value: prevState.value + 1 }));  
};
```

This way we increment the value, instead of re-writing it completely.

- Each time we update the state, React creates new state objects, and just populates it with previous data and new updated fields


- State should be stored in the closest parent for the elements that require access to that state