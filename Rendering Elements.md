# Rendering elements

## What is an elements?
1. Smallest building blocks of React
2. They make up components
3. They dictate what we see on the screen

## How are elements rendered?
1. We identify a root node in the DOM

Somewhere in the markup there is: `<div id = "root">...</div>`
We fetch it using: 
`const ele = document.getElementById(root)`

2. Then we use ReactDOM.createRoot() on it to make it a React DOM root [Usually there is just one root node, but some applications can have multiple isolated roots]

`const root = ReactDOM.createRoot(ele)`

3. Then we use root.render() with arguments as what is to be rendered. Eg: rendering an element:

```
const rederingEle = "Hello World"
root.render(renderingEle)
```

## Selective rendering
1. React elements are immutable
2. Whenever render() is called, ReactDOM compares it and its children to the previous state, and only updates the main DOM if there is a change - This is why React is fast
