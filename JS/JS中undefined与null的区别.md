## JS中undefined与null的区别

- undefined表示一个变量没有被声明，或者被声明但没有被赋值。

  ```javascript
  var a;
  console.log(a);    // undefined
  
  var dict={'a':'one'};
  console.log(dict['a']);    // one
  console.log(dict['b']);    // undefined
  ```

- undefined如果一个函数什么都不返回，则该函数默认返回undefined。

  ```javascript
  console.log(test());    // undefined
  function test(){
  	alert('test');
  }
  ```

- undefined和null的值相等，但类型不等：undefined的类型（typeof）是undefined；null的类型是object。

  ```javascript
  null==undefined    // true
  null===undefined    // false
  typeof(undefined)    // undefined
  typeof(null)    // object
  typeof(NaN)    // number
  ```

- undefined转换为数字类型时值为NaN，null转换为数字类型时值为0。

  ```javascript
  console.log(Number(null));    // 0
  console.log(Number(undefined));    // NaN
  console.log(5+null);    // 5
  console.log(5+undefined);    // NaN
  console.log(5+NaN);    // NaN
  ```
