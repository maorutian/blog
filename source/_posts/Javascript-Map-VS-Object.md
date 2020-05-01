---
title: 'Javascript: Map VS Object'
date: 2020-04-30 19:19:47
categories: 
- Javascript
tags:
- Javascript
- Map
- Object
---
`Map` and `Object` both are data collection types, they all store key-value pairs.

### Difference

#### Key type
* The keys MUST be String in `Object`. See [Property Accessor docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_Accessors)

> Property names must be strings. This means that non-string objects cannot be used as keys in the object. Any non-string object, including a number, is typecasted into a string via the toString method

<!-- more -->

Example:

```
> var foo = {}
undefined

> foo[23213] = 'swag'
'swag'

> foo
{ '23213': 'swag' }

> typeof(Object.keys(foo)[0])
'string'

```

* But in `Map` it can be ANY data type.

#### Element order
* The Elements in `Map `are ordered. Thus, when iterating over it, a Map object returns keys in order of insertion.

* The Elements of an `Object` are not ordered

#### Inheritance
* Map is an instance of `Object `.
* `Object ` is not an instance of `Map`.


### When to use Map

#### loop through

 `Map` is mainly used for fast searching and looking up data.
 
 For `Object `, if you want to loop through keys、values and entries, you have to convert Object to Array using `Object.keys()`、`Object.values()` and `Object.entries()`，or using `for ... in`. But a for...in loop only iterates over enumerable, non-Symbol properties, and the order is random.
 
A `Map` is an iterable, so it can be directly iterated.We can use `for ... of` or `forEach`.

```
 for (let [key, value] of map) {
  console.log(key);
  console.log(value);
};
map.forEach((key, value) => {
  console.log(key);
  console.log(value);
});
```

Besides, you can use `map.size` to get `length`. but you have to convert Object to Array in object and then use `Object.keys({}).length`

#### Lots of Add and delete operations
`Map` is purely hash, in scenarios that requires a lot of adding and removing (especially) new pair, `Map` may perform much better.

#### Large set of data
`Map` tends to perform better in storing large set of data, especially when keys are unknown until run time, and when all keys are the same type and all values are the same type.

### when to use object
#### Separate logic to individual property
You variable need separate logic to different property, `Object ` is the choice. `Map` doesn't support it.

```
var obj = {
    id: 1, 
    name: "It's Me!", 
    print: function(){ 
        return `Object Id: ${this.id}, with Name: ${this.name}`;
    }
}
console.log(obj.print());//Object Id: 1, with Name: It's Me.


```

#### JSON
JSON has support for `Object `, but not with `Map` (yet). So in certain situation where we have to work a lot with JSON, consider `Object ` as preferred option.




