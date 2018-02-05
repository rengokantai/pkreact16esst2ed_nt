# pkreact16esst2ed_nt

## 1. What's New
React is performant because it minimizes the number of DOM operations it has to 
invoke by reconciling changes in a render tree


## 3. Creating Your First React Element
How virtual DOM works
- Whenever a state of your data model changes, the virtual DOM and React will rerender
your UI to a virtual DOM representation.
- It then calculates the difference between the two virtual DOM representations: the previous virtual 
DOM representaion that was computed before the data was changed and the current virtual DOM representation that was
computed after data was changed.
- The difference between the two virtual DOM representations is what actually needs to be changed in the real DOM.



#### Parameters
```
React.createElement(type,props,children)
```


React.createFactory
```
const createListElement = React.createFactory('li');
const listItemElement = createListElement({className:'ke',key:'item'},'Item1');
```

React.DOM.li, React.DOM.div

## 4. Creating Your First React Component
###### pg78
There are two ways to pass data to a render() method using the react API
```
this.props
this.state
```

It is a good practice to keep as many React components stateless as possible

##### difference
this.state, this.props
- this.props: This stores read-only data that is passed from the parent. It belongsto the parent and cannot be changed by its 
children. Immutable
- this.state: Is private to the component. It can be changed by the component. The component will re-render itself when
the state is updated


##### setState
```
this.setState(prevState=>({
  isHeaderHidden:!prevState.isHeaderHidden
}))
```

React does not create an inline event handler in the rendered HTML markup.
This is because React doesnot actually attach event handlers to the DOM nodes themselves

##### What if we move the ```isHeaderHidden``` prpoerty out of our state object
because our ```render()``` method will not be triggered automatically by React every time


## 5. Making Your React Components Reactive
```
import ReactDOMServer from 'react-dom/server';
ReactDOMServer.renderToString()
ReactDOMServer.renderToStaticMarkup
```

###### 103
Notice that the ```Collection``` Component cannot directly mutate the ```Application``` component state. The ```Collection``` component has read only access to the state via a ```this.props``` object.  
The only way to update the parent component's state is to call the callback functions that are passed by a parent component.


###### 112
###### 116
Inserting a component into the DOM is called `mounting`, whereas removing a component from the DOM is called `unmounting`
