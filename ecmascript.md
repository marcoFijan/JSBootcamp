#ECMAScript
ECMAScript is the standard upon which JavaScript is based, and it’s often abbreviated to ES.

**TC39** is the committee that evolves JavaScript. The members are companies involved in JavaScript and browsers (Mozilla, Google, Facebook, Apple, Microsoft, Intel, Paypal, Salesforce, etc)

| Edition                | Official name | Date published      |
| ---------------------- |---------------|---------------------|
| ES.Next                | ES.Next       | *Future*            |
| ES11 (cur ES.Next)     | ES2020        | Summer 2020?        |
| ES10                   | ES2019        | Summer 2019         |
| ES9                    | ES2018        | June 2018           |
| ES8                    | ES2017        | June 2017           |
| ES7                    | ES2016        | June 2016           |
| ES6                    | ES2015        | June 2015           |
| ES5.1                  | ES5.1         | June 2011           |
| ES5                    | ES5           | December 2009       |
| ES4                    | ES4           | Abandoned           |
| ES3                    | ES3           | December 1999       |
| ES2                    | ES2           | June 1998           |
| ES1                    | ES1           | June 1997           |

**Don’t use the edition names. But use the official names.**

JavaScript gots his name because the word Script was popular at the time and they wanted to attract mostly Java developers. It’s got nothing to do with Java.

##Variables
Since ES6 there are different variables:

###Var
Vars are accessible outsite of loops. When you make a variable in a for-loop, that variable will be accessible outsite the  for-loop.

If there is no variable visable within a function, it will go search all the way up the code.

```javascript
function(){
  for(i = 0; i < 10; i++){
    console.log(i);
  }
}
```

There is no variable i so javascript checks the code upwards. Cannot find an i variable, so makes one:

```javascript
var i;

function(){
  for(i = 0; i < 10; i++){
    console.log(i);
  }
}
```

When you use the **use stric** statement on top, it won’t make the variable. Always use this on top of your javascript!

##Let
Will only be accessible inside the for-loop or if-statement.
Let should be the new var. That way you use the variables the same as in other programminglanguages.
**Var shouldn’t be used anymore.**

##Const
Const is almost the same as let, but const can’t be reassigned. But you can change a property of const:

**ERROR**
```javascript
Const x = 5
X = 6
```

**POSSIBLE**
```javascript
Const x = {y: 5}
x.y = 6
```

Always use const when you don’t need to change the variable because of: **minimize mutable state**.
