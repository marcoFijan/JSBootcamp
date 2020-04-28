# Functions
Why use functions?
..* Modularity - Functions are a way to organize your code.
..* Reusibility - Reuse the function to make difficult tasks easier.

Split functions into small tasks. That way you have more modularity and more control of your code.

When there is a **return** without an expression, or when there is no return statement at all, the function will return *undefined*

Binding visibility (with let) is called **lexical scoping**

Let bindings that binds a function, can still be overwritten:
```javascript
let launchMissiles = function() {
  missileSystem.launch("now");
};
if (safeMode) {
  launchMissiles = function() {/* do nothing */};
}
```

A method is a function in an object
