# Data Structures
Arrays can be made in Javascript by:
```javascript
Let listOfNumbers = [1, 3, 5, 7];
Console.log(listOfNumbers[3]);
```
Begint bij 0. Member?

An object exists in a key and a value like;
key1: ‘value’,’
key2: 12,
key3: [{
	key: ‘value’,
	key: ‘value’
}],

##Objects
One way to make an object is by using { }
```javascript
let day1 = {
  squirrel: false,
  events: ["work", "touched tree", "pizza", "running"]
};
console.log(day1.squirrel);
// → false
console.log(day1.wolf);
// → undefined
day1.wolf = false;
console.log(day1.wolf);
// → false
```
You can then add an property by calling the object and putting a . behind it.

The delete operator cuts off a tentacle from an ‘octopus’. (objects are like octopuses with any number of tentacles, each of which has a name tattooed on it).
```javascript
let anObject = {left: 1, right: 2};
console.log(anObject.left);
// → 1
delete anObject.left;
console.log(anObject.left);
// → undefined
console.log("left" in anObject);
// → false
console.log("right" in anObject);
// → true
```

To find out which properties are in one object, you can use Object.keys
```javascript
console.log(Object.keys({x: 0, y: 0, z: 2}));
// → ["x", "y", "z"]
```

## Edit Objects
There’s an Object.assign function that copies all properties from one object into another.
```javascript
let objectA = {a: 1, b: 2};
Object.assign(objectA, {b: 3, c: 4});
console.log(objectA);
// → {a: 1, b: 3, c: 4}
```

If you want to overwrite an single arrayvalue:
```javascript
anArray[1] = “Marieke”
```

To edit a key within an array you can:
```javascript
anArray[1][“hair Colour”] = “bruin”		wanneer er een spatie is
anArray[1].hairCollor = “bruin”			wanneer er geen spatie is
```

You can make a specific for-loop for objects as well:
```javascript
function inspectObject(obj){
  for (var keyName in obj){
    console.log("Key: ", keyName, "Value: ", obj[keyName])
  }
  inspectObject(newMarieke)
}
```

## Calling Values
```javascript
let object1 = {value: 10};
let object2 = object1;
let object3 = {value: 10};

console.log(object1 == object2);
// → true
console.log(object1 == object3);
// → false

object1.value = 15;
console.log(object2.value);
// → 15
console.log(object3.value);
// → 10
```

In the tableFor function, there is a loop like this
```javascript
for (let i = 0; i < JOURNAL.length; i++) {
  let entry = JOURNAL[i];
  // Do something with entry
}
```
But it can also be written like this:
```javascript
for (let entry of JOURNAL) {
  console.log(`${entry.events.length} events.`);
}
```

## Mapping
When you need a map whose keys can’t easily be converted to strings, such as objects, you cannot use an object as your map.
Instead, use the method Map().
```javascript
let ages = new Map();
ages.set("Boris", 39);
ages.set("Liang", 22);
ages.set("Júlia", 62);

console.log(`Júlia is ${ages.get("Júlia")}`);
// → Júlia is 62
console.log("Is Jack's age known?", ages.has("Jack"));
// → Is Jack's age known? false
console.log(ages.has("toString"));
// → false
```

## Back to Arrays
It is possible to put an array into an array
```javascript
let journal = [
  {events: ["work", "touched tree", "pizza",
            "running", "television"],
   squirrel: false},
  {events: ["work", "ice cream", "cauliflower",
            "lasagna", "touched tree", "brushed teeth"],
   squirrel: false},
  {events: ["weekend", "cycling", "break", "peanuts",
            "beer"],
   squirrel: true},
  /* and so on... */
```
