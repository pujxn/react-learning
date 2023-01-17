# JSX

## WHY JSX?
1. JSX produces react elements
2. JSX is compiled into JS functions that return JS objects- so you can use it as you would another funciton call
3. JSX serves as a visual aid for markup by coupling in with rendering logic

## Embedding JS expressions in JSX
1. Any expression to be wrapped in curly braces
2. String literals to have just quotes around it

## Specifying attributes for JSX tags
Eg: `const element = <a href="https://www.reactjs.org"> link </a>;`   --> Using a string literal
Eg: `const element = <img src={user.avatarUrl}></img>;`  --> Using a JS expression


## JSX prevents injection attacks
1. Everything in JSX is treated as a string, and even special characters like "<>", "()" are escaped

## JSX compilation:
1. Babel compiles JSX into JS
2. JSX elements are converted to React.createElement function calls. Eg: 

```const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
); ``` 

**BECOMES**

```const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);```

**WHICH RETURNS**

```const element = {
  type : "h1",
  props: {
    className: "greeting",
    children: "Hello, world!"
  }
}```

## TIPS: 
1. Wrap JSX in parantheses to avoid automatic semicolon insertion
2. In JSX 'class' attribute --> 'className' to avoid collision with JS class keyword
3. Attributes in JSX follow camel case, Eg: tabindex --> tabIndex [Because JSX is closer to JS than it is to HTML]
4. In JSX, whatever comes between an opening and closing tag is the child of that element. Even if it's a string. Eg:
<h1> Hello </h1> -> Here, "Hello" is a child of h1 element

