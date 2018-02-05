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
