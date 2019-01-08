## TODO:

1. 嵌套？
2. 强制转换？

## Reference

- https://stackoverflow.com/questions/1889014/can-i-construct-a-javascript-object-without-using-the-new-keyword
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty

## Usage 

```javascript
// https://stackoverflow.com/questions/1889014/can-i-construct-a-javascript-object-without-using-the-new-keyword
function SomeConstructor(){
   if (!(this instanceof SomeConstructor)){
        return new SomeConstructor();
   }
   //the constructor properties and methods here
}
```

```javascript
import {Schema, Types} from 'js-schema'

const Person = Schema({
  name: Types().default('').string().isRequired()
})

const person = Person({
  name: 'liguangyi'
})

```

### Type

string, number, boolean, object, array, regex

### Property

default, isRequired, valueOf

