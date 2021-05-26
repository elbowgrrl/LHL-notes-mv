# Object Literals
## Object Literals
- A non-primitive data type, often used to store more complex data and methods.
- contain key/value pairs. Each key in an object is unique ```{key: value}```
- Object keys are always strings (or symbols[uncommon])
- Object values can be any type (Primitive or non-primitive, including other objects.)

``` 
const exampleObj = {

name: "myObj",
JavascriptObject: true,
numberOfExamples: 1,
iCanHaveAChildObj: { possible: true},
method: function() {
  console.log("I'm a function on an object which is called a method")
};

}
```

## Accessing Object Values
Accessing values when you know they key name is simple. Just type the name of the object, the dot oporator and the name of the key.
``` 
exampleObj.name

returns "myObj"
```
This can also be done by using bracket notation 
```
exampleObj["name"]

returns "myObj"
```
## Accessing Object Keys
Accessing the names of Object keys is not as streight forward, but there are some strategies. There are some factory functions which can do the job, but I will also outline some strategies below.
Using the ***Object.keys()*** method will return an array of object keys which can then be accessed by their array index.
```
const obj = {
  name: "object",
  type: true,
  anothervalue: "string"
};

let objName = Object.keys(obj)

console.log(objName[0]);

returns "name"
```

An Object can also be iterated over to access the names of the keys directly using a ***for...in*** loop. In this case, the key in an object acts like indices would in an array. Therefore, upon iteration they keys can be accessed with the iterator.
```
const obj = {
  name: "object",
  type: true,
  anothervalue: "string"
};

for (let keys in obj) {
  console.log(keys)
}

returns

name
type
anotherValue

/// AND ////

for (let key in obj) {
  if (obj[key] === true) {
    console.log(key);
    console.log(obj[key]);
  }
}

returns
type
true
```

## Adding Values to Objects
 You can add new values to existing keys or add a new key value pair in the same way. 
 ```
 const obj = {
  name: "object",
  type: true,
  anothervalue: "string"
};

obj["type"] = false;
obj["yetAnotherValue"] = "puppy";

console.log(obj);

returns

{
  name: 'object',
  type: false,
  anothervalue: 'string',
  yetAnotherValue: 'puppy'
}
```


