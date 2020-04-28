# Value types

## Numbers
| Number        | Meaning                                          |
| ------------- |--------------------------------------------------|
| 9.81          | Fractional Numbers                               |
| 981           | Integer                                          |
| 2.998e8       | 2.998 x 108 = 299,800,800                        |
| Infinity      | Positive infinity                                |
| -Infinity     | Negative infinity                                |
| NaN   	      | Not a Number (when 0 / 0 or Infinity – Infinity) |

1. ()
2. e9
3. * /
4. +-

## Strings
| Formatting    | Meaning                                                                            |
| ------------- |------------------------------------------------------------------------------------|
| \n            | New line within a String: "This is a \nNew line"                                   |
| \t            | New tab within a string                                                            |
| \\            | Two backslashes will collapse together which will result in a single \ in a string |
| ${int}        | Result will be computed and converted to string                                    |

## Unary Operator
Typeof 		= 	Naming the type of value: console.log(typeof 4.5) > number

## Boolean Values
| Code          | Value                                                                              |
| ------------- |------------------------------------------------------------------------------------|
| Console.log(3 > 2)                      | will give a Boolean value true since it is true          |
| Console.log(“Aardvard” < “Zoroaster”)   | New tab within astring                                   |

Javascript will read strings with < and > as follows:

‘less’-------------------------------------‘greater’
ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz

**Javascript berekent eerst de statements en functions, en maakt daarna pas de variable en / of function aan en staat de waarde op.**

## Logical Operator
| Operator | Meaning                                          |
| -------- |--------------------------------------------------|
| &&       | And 	(both must be true)                         |
| ||       | Or	  (one must be true)                          |
| !false   | true                                             |
| !true    | false                                            |
| ==       | value is equal to                                |
| ===      | is exactly the same                              |
| !=       | is Not                                           |
| !==      | is not equal to                                  |
| <        | is smaller than                                  |
| >        | is greater than                                  |
| <=       | is smaller than or equal to                      |
| >=       | is greater than or equal to                      |

If you give 2 valid values with or ( || ), then it will try to first use the first value. If that one is null or invalid, it will try to use the second one:
console.log(null || "user")			    	// → user
console.log("Agnes" || "user")				// → Agnes
This way, you can fall back on a default value if the new value is corrupt or invalid.

## Empty Values
Null		  =	empty
Undefined	=	empty
Null is your doing: var I = null;
Undefined is an error in in the code / console: Warning I is undefined

## Automatic type conversion
Javascript is smarter than Java and will try to convert values in to readable values when needed:

```javascript
console.log(8 * null)		// → 0
console.log("5" - 1)		// → 4
console.log("5" + 1)		// → 51
console.log("five" * 2)		// → NaN
console.log(false == 0)		// → true
```
