# Block scope variables

```javascript
var foo = 'bar';

if(foo) {
  let foo = 'baz'
  console.log('inside if:', foo); // Should equal 'baz'
}
console.log(foo); // Should equal 'bar'
```

# Constants

```javascript
const TryAndOverwriteMe = 'Stubborn';

try {
  TryAndOverwriteMe = 'Take this!';
}
catch(err) {
  console.log(err);
}
```

# Classes

```javascript
class Person {
  constructor(name = 'Lourdes') {
    this.name = name;
  }
  say(){
    return 'Hi, my name is ' + this.name;
  }
}
```
```javascript
var justin = new Person('Justin');
justin.say(); // Outputs 'Hi, my name is Justin'

var lourdes = new Person(); // Will use constructor's default
lourdes.say(); // Outputs 'Hi, my name is Lourdes'
```

## Extending a class

```javascript
class SuperHero extends Person {
  constructor(name) {
    super(name)
  }
  fly() {
    return this.name + ' is flying';
  }
  static flyHigher() {
    return this.name + ' flying like an eagle'
  }
}
```
```javascript
var superJustin = new SuperHero('SuperJustin');
superJustin.fly(); // Outputs 'Justin' is flying
```

# Enhanced Objects

```javascript
var obj = {
  thisIsAMethod() {
    return 'Boom';
  }
}
```

# Strings

## Template strings

### String interpolation
```javascript
var superlative = 'fanbloodytastic';
var template = `ES6'\s ${superlative} string interpolation`;
```

### Multiline strings
```javascript
var template `...and it also
allows
multiline
strings`;
```

# Functions

## Arrow Functions

```javascript
let add = (a,b) => { return a + b }
console.log(add(1,2));
```

## Static methods

```javascript
var superDuperJustin = new SuperHero('SuperDuperJustin');
superDuperJustin.flyHigher(); // Should return undefined
SuperHero.flyHigher(); // Should return 'flying like an eagle'
```

