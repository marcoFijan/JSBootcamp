# Concepts

## Global and Fases
Met het woordje **this** krijg je je huidige **global object** het is ook mogelijk om in plaats van **this**, **window** te gebruiken om specifiek het global object in de window aan te roepen.
Wanneer er gebruikt gemaakt wordt van nodeJS, kun je het globale object aanroepen door **global**

Javascript leest eerst de codes en slaat alle variables en function declarations op in memory. Daarna leest hij het nog een keer en vult de gegevens ook daadwerkelijk in course = ‘block tech’ Het assignen gebeurd dus pas in de **execution fase**. (2de keer lezen na **creation fase**)

## Hoisting
Alle variable declarations (var = “string”) zet hij bovenaan
Alleen de declarations worden bovenaan gezet. Niet de assignments:

```javascript
Console.log(num);
Var num;
Num = 6;
```

*wordt...*

```javascript
Var num;
Console.log(num)
Var = 6
```

En dus komt er *undefined* uit

## Closure
Functions in functions kunnen alle functions boven in de keten bereiken tot aan de global scope.
Functions in een functions worden ook wel **inner functions** genoemd.
Closures laten toe dat de **inner function** de variablen kan bereiken of zijn **outer function**:

```javascript
//global scope
var henk1 = "henk1"

function func1(){
  //local scope
  var henk2 = "henk2"

  function func2(){
    //local scope
    var henk3 = "henk3"

    function func3(){
      //local scope
      var henk 4 = "henk4"

      console.log(henk1);
    }
  }
}
```

## Scope
De huidige context

### Global Scope
De window in de browser (niet in een window een variable aanmaakt, wanneer er geen function omheen zit) window.variablenaam is mogelijk wanneer de variable in de global scope zit. (iedereen kan bij het window object en dus is het de global scope)

*Versus...*

### Local scope
Elke keer als je een function declaration doet, krijg je een nieuwe local scope. De data in de function, hoort dus bij de scope, van die function.

*****************************************

### Function scope
Binnen een function declaration wordt het een function scope.
Local en function scope zijn vrijwel hetzelfde. Wanneer je het echt over de function hebt en de scope daarvan, dan is het een function scope, maar als je het alleen over de code daarbinnen hebt, is het een local scope

*Versus...*

### Block Scope
Binnen een niet function statement. Zoals if-statement en for-loop. (binnen curly braces {} met eventuele label)

Voorbeeld:
```javascript
//global

function greetings(){
  //function scope / Local Scope
  var henk = "henk" // function scope / Local Scope

  if(true){ //block scope, GEEN nieuwe local scope
    let henk2 = "henk2" //block scope
  }

  console.log(henk); //henk
  console.log(henk2); //ERROR, henk2 not defined
}
```
