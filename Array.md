#                                                                      Array

###     Array属性

#### .constructor()

#####  .constructor: function Array()   返回创建数组对象的原型函数。

- ##### 语法

  ```
  array.constructor 
   返回值是函数的引用，不是函数名：
  JavaScript 数组 constructor 属性返回 function Array() { [native code] }
  JavaScript 数字 constructor 属性返回 function Number() { [native code] }
  JavaScript 字符串 constructor 属性返回 function String() { [native code] }
  如果一个变量是数组你可以使用 constructor 属性来定义。
  ```

- ###### 返回值

  ```
  一个函数对象。该函数由数组对象的原始创建。
  ```

- ###### 参数

  ```
  无
  ```

  

- ###### 实例

  ```
  返回fruits数组对象原型创建的函数：
  fruits.constructor;
  结果输出：
  function Array() { [native code] }
  ```


####  length()  

##### function length()    设置或返回数组元素的个数。

- ###### 语法

  ```
  设置数组的数目：
  array.length=number
  
  Return the length of an array:
  array.length
  
  length 属性可设置或返回数组中元素的数目。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  一个数字，表示数组中的对象的元素数目。
  ```

- ###### 实例

  ```
  返回数组的数目：
  fruits.length;
  
  The result could be
  4
  ```

#### prototype 

##### prototype    允许你向数组对象添加属性或方法。

- ###### 语法

  ```
  Array.prototype.name=value
  
  prototype 属性使您有能力向对象添加属性和方法。
  当构建一个属性，所有的数组将被设置属性，它是默认值。
  在构建一个方法时，所有的数组都可以使用该方法。
  注意： Array.prototype 单独不能引用数组, Array() 对象可以。
  注意： 在JavaScript对象中，Prototype是一个全局属性。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  无
  ```

- ###### 实例

  ```
  一个新的数组的方法，将数组值转为大写：
  Array.prototype.myUcase=function()
  {
      for (i=0;i<this.length;i++)
      {
          this[i]=this[i].toUpperCase();
      }
  }
  
  创建一个数组，然后调用 myUcase 方法：
  var fruits=["Banana","Orange","Apple","Mango"];
  fruits.myUcase();
  
  fruits 数组现在的值为：
  BANANA,ORANGE,APPLE,MANGO 
  ```

  

###        Array方法

#### .concat()

#####  .concat: function concat()     连接两个或更多的数组，并返回结果。

-         ###### 语法

  ```
  array1.concat(array2,array3,...,arrayX);
  用于连接两个或多个数组。该方法不会改变现有的数组，而仅仅会返回被连接数组的一个副本
  ```

- ###### 参数

  ```
  array2,array3,...,arrayX
  ```

-         ###### 返回值

  ```
  返回一个新的数组。该数组是通过把所有 arrayX 参数添加到 arrayObject 中生成的。如果要进行 concat() 操作的参数是数组，那么添加的是数组中的元素，而不是数组。
  ```

-         ###### 实例

  ```
  var hege = ["Cecilie", "Lone"];
  var stale = ["Emil", "Tobias", "Linus"];
  var kai = ["Robin"];
  var children = hege.concat(stale,kai);
   输出结果：Cecilie,Lone,Emil,Tobias,Linus,Robin 
  ```

  

####  copyWithin()

#####  copyWithin: function copyWithin()  从数组的指定位置拷贝元素到数组的另一个指定位置中。

- ###### 语法

  ```
  array.copyWithin(target, start, end)
  ```
  
- ###### 参数

  ```
  target 	必需。复制到指定目标索引位置。
  start 	可选。元素复制的起始位置。
  end 	可选。停止复制的索引位置 (默认为 array.length)。如果为负值，表示倒数。
  ```

- ###### 返回值

  ```
  数组
  ```
  
- ###### 实例

  ```
  复制数组的前面两个元素到后面两个元素上：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.copyWithin(2, 0);
  
  fruits 输出结果：
  Banana,Orange,Banana,Orange 
  ```

  

#### entries()

##### entries: function entries()  返回数组的可迭代对象。

- ###### 语法

  ```
  array.entries()
  entries() 方法返回一个数组的迭代对象，该对象包含数组的键值对 (key/value)。
  迭代对象中数组的索引值作为 key， 数组元素作为 value。
  ```

- ###### 参数

  ```
  没有参数。
  ```

- ###### 返回值

  ```
  数组迭代对象
  ```

- ###### 实例

  ```
  从数组 fruit 创建一个可迭代对象， 该对象包含了数组的键值对：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.entries();
  ```



#### every()

##### every: function every()    检测数值元素的每个元素是否都符合条件。

- ###### 语法

  ```
  array.every(function(currentValue,index,arr), thisValue)
  
  every() 方法用于检测数组所有元素是否都符合指定条件（通过函数提供）。
  every() 方法使用指定函数检测数组中的所有元素：
      如果数组中检测到有一个元素不满足，则整个表达式返回 false ，且剩余的元素不会再进行检测。
      如果所有元素都满足条件，则返回 true。
  注意： every() 不会对空数组进行检测。
  注意： every() 不会改变原始数组。
  ```

- ###### 参数

  ```
  currentValue 	必须。当前元素的值
  index 	可选。当前元素的索引值
  arr 	可选。当前元素属于的数组对象
  thisValue 	可选。对象作为该执行回调时使用，传递给函数，用作 "this" 的值。如果省略了 thisValue,					"this" 的值为 "undefined"
  ```

- ###### 返回值

  ```
  布尔值。如果所有元素都通过检测返回 true，否则返回 false。
  ```

- ###### 实例

  ```
  检测数组 ages 的所有元素是否都大于等于 18 :
  var ages = [32, 33, 16, 40];
  
  function checkAdult(age) {
      return age >= 18;
  }
  
  function myFunction() {
      document.getElementById("demo").innerHTML = ages.every(checkAdult);
  }
  
  输出结果为:
  false
  ```



#### .fill() 

##### fill: function fill()  使用一个固定值来填充数组。

- ###### 语法

  ```
  array.fill(value, start, end)
  fill() 方法用于将一个固定值替换数组的元素。
  ```

- ###### 参数

  ```
  value 	必需。填充的值。
  start 	可选。开始填充位置。
  end 	可选。停止填充位置 (默认为 array.length)
  ```

- ###### 返回值

  ```
   数组
  ```

- ###### 实例

  ```
  使用固定值填充数组：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.fill("Runoob");
  
  fruits 输出结果：
  Runoob,Runoob,Runoob,Runoob 
  ```

  

####  filter()

##### filter: function filter()  检测数值元素，并返回符合条件所有元素的数组。

- ###### 语法

  ```
  array.filter(function(currentValue,index,arr), thisValue)
  
  filter() 方法创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
  注意： filter() 不会对空数组进行检测。
  注意： filter() 不会改变原始数组。
  ```

- ###### 参数

  ```
  currentValue 	必须。当前元素的值
  index 	可选。当前元素的索引值
  arr 	可选。当前元素属于的数组对象
  thisValue 	可选。对象作为该执行回调时使用，传递给函数，用作 "this" 的值。
  如果省略了 thisValue ，"this" 的值为 "undefined"
  ```

- ###### 返回值

  ```
   	返回数组，包含了符合条件的所有元素。如果没有符合条件的元素则返回空数组。
  ```

- ###### 实例

  ```
  var ages = [32, 33, 16, 40];
  
  function checkAdult(age) {
      return age >= 18;
  }
  
  function myFunction() {
      document.getElementById("demo").innerHTML = ages.filter(checkAdult);
  }
  输出结果为:
  32,33,40
  ```

  

#### find()

##### find: function find()	返回符合传入测试（函数）条件的数组元素。

- ###### 语法

  ```
  array.find(function(currentValue, index, arr),thisValue)
  
  find() 方法返回通过测试（函数内判断）的数组的第一个元素的值。
  find() 方法为数组中的每个元素都调用一次函数执行：
      当数组中的元素在测试条件时返回 true 时, find() 返回符合条件的元素，之后的值不会再调用执行函数。
      如果没有符合条件的元素返回 undefined
  
  注意: find() 对于空数组，函数是不会执行的。
  注意: find() 并没有改变数组的原始值。
  ```

- ###### 参数

  ```
  currentValue 	必需。当前元素
  index 	可选。当前元素的索引值
  arr 	可选。当前元素所属的数组对象
  thisValue 	可选。 传递给函数的值一般用 "this" 值。
  					如果这个参数为空， "undefined" 会传递给 "this" 值
  ```

- ###### 返回值

  ```
  返回符合测试条件的第一个数组元素值，如果没有符合条件的则返回 undefined。
  ```

- ###### 实例

  ```
  获取数组中年龄大于 18 的第一个元素
  var ages = [3, 10, 18, 20];
   
  function checkAdult(age) {
      return age >= 18;
  }
   
  function myFunction() {
      document.getElementById("demo").innerHTML = ages.find(checkAdult);
  }
  
  fruits 输出结果：
  18 
  ```

  

#### findIndex()

##### findIndex: function findIndex()   返回符合传入测试（函数）条件的数组元素索引

- ###### 语法

  ```
  array.findIndex(function(currentValue, index, arr), thisValue)
  
  findIndex() 方法返回传入一个测试条件（函数）符合条件的数组第一个元素位置。
  findIndex() 方法为数组中的每个元素都调用一次函数执行：
      当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
      如果没有符合条件的元素返回 -1
  
  注意: findIndex() 对于空数组，函数是不会执行的。
  注意: findIndex() 并没有改变数组的原始值。
  ```

- ###### 参数

  ```
  currentValue 	必需。当前元素
  index 	可选。当前元素的索引
  arr 	可选。当前元素所属的数组对象
  thisValue 	可选。 传递给函数的值一般用 "this" 值。
  如果这个参数为空， "undefined" 会传递给 "this" 值
  ```

- ###### 返回值

  ```
   	返回符合测试条件的第一个数组元素索引，如果没有符合条件的则返回 -1。
  ```

- ###### 实例

  ```
  获取数组中年龄大于等于 18 的第一个元素索引位置
  var ages = [3, 10, 18, 20];
   
  function checkAdult(age) {
      return age >= 18;
  }
   
  function myFunction() {
      document.getElementById("demo").innerHTML = ages.findIndex(checkAdult);
  }
  
  fruits 输出结果：
  2 
  ```

  





#### flat()  

##### flat: function flat()  按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的子数组中的元素合并为一个									新数组返回。

- ###### 语法

  ```
  var newArray = arr.flat([depth])
  
  flat() 方法会按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的子数组中的元素合并为一个新数组返回。
  ```

- ###### 参数

  ```
  
  depth 可选
      指定要提取嵌套数组的结构深度，默认值为 1。 
  ```

- ###### 返回值

  ```
  一个包含将数组与子数组中所有元素的新数组。
  ```

- ###### 实例

  ```
  var arr1 = [1, 2, [3, 4]];
  arr1.flat(); 
  // [1, 2, 3, 4]
  
  var arr2 = [1, 2, [3, 4, [5, 6]]];
  arr2.flat();
  // [1, 2, 3, 4, [5, 6]]
  
  var arr3 = [1, 2, [3, 4, [5, 6]]];
  arr3.flat(2);
  // [1, 2, 3, 4, 5, 6]
  
  //使用 Infinity 作为深度，展开任意深度的嵌套数组
  arr3.flat(Infinity); 
  // [1, 2, 3, 4, 5, 6]
  
  var arr4 = [1, 2, , 4, 5];
  arr4.flat();
  // [1, 2, 4, 5]
  ```

  

#### flatMap()

##### flatMap: function flatMap()   首先使用映射函数映射每个元素，然后将结果压缩成一个新数组。

- ###### 语法

  ```
  flatMap() 方法首先使用映射函数映射每个元素，然后将结果压缩成一个新数组。它与 map 和 深度值1的 flat 几乎相同，但 flatMap 通常在合并成一种方法的效率稍微高一些。
  ```

- ###### 参数

  ```
  
  callback
      可以生成一个新数组中的元素的函数，可以传入三个参数：
  
      currentValue
          当前正在数组中处理的元素
      index可选
          可选的。数组中正在处理的当前元素的索引。
      array可选
          可选的。被调用的 map 数组
  
  thisArg可选
      可选的。执行 callback 函数时 使用的this 值。
  
  返回值
  ```

- ###### 返回值

  ```
  一个新的数组，其中每个元素都是回调函数的结果，并且结构深度 depth 值为1。
  ```

- ###### 实例

  ```
  var arr1 = [1, 2, 3, 4];
  
  arr1.map(x => [x * 2]); 
  // [[2], [4], [6], [8]]
  
  arr1.flatMap(x => [x * 2]);
  // [2, 4, 6, 8]
  
  // 只会将 flatMap 中的函数返回的数组 “压平” 一层
  arr1.flatMap(x => [[x * 2]]);
  // [[2], [4], [6], [8]]
  
  let arr = ["今天天气不错", "", "早上好"]
  
  arr.map(s => s.split(""))
  // [["今", "天", "天", "气", "不", "错"],[],["早", "上", "好"]]
  
  arr.flatMap(s => s.split(''));
  // ["今", "天", "天", "气", "不", "错", "早", "上", "好"]
  ```

  

#### forEach()

##### forEach: function forEach()	数组每个元素都执行一次回调函数。

- ###### 语法

  ```
  array.forEach(function(currentValue, index, arr), thisValue)
  
  forEach() 方法用于调用数组的每个元素，并将元素传递给回调函数。
  注意: forEach() 对于空数组是不会执行回调函数的。
  ```

- ###### 参数

  ```
  currentValue 	必需。当前元素
  index 	可选。当前元素的索引值。
  arr 	可选。当前元素所属的数组对象。
  thisValue 	可选。传递给函数的值一般用 "this" 值。
  如果这个参数为空， "undefined" 会传递给 "this" 值
  ```

- ###### 返回值

  ```
   	undefined
  ```

- ###### 实例

  ```
  列出数组的每个元素：
  <button onclick="numbers.forEach(myFunction)">点我</button>
  <p id="demo"></p>
   
  <script>
  demoP = document.getElementById("demo");
  var numbers = [4, 9, 16, 25];
   
  function myFunction(item, index) {
      demoP.innerHTML = demoP.innerHTML + "index[" + index + "]: " + item + "<br>"; 
  }
  </script>
  
  输出结果：
  index[0]: 4
  index[1]: 9
  index[2]: 16
  index[3]: 25 
  ```

  

####  includes()

##### includes: function includes()	判断一个数组是否包含一个指定的值。

- ###### 语法

  ```
  arr.includes(searchElement)
  arr.includes(searchElement, fromIndex)
  
  includes() 方法用来判断一个数组是否包含一个指定的值，如果是返回 true，否则false。
  ```

- ###### 参数

  ```
  searchElement 	必须。需要查找的元素值。
  fromIndex 	可选。从该索引处开始查找 searchElement。如果为负值，则按升序从 array.length + fromIndex 的索引开始搜索。默认为 0。
  ```

- ###### 返回值

  ```
   	布尔值。如果找到指定值返回 true，否则返回 false。
  ```

- ###### 实例

  ```
  检测数组 site 是否包含 runoob :
  let site = ['runoob', 'google', 'taobao'];
   
  site.includes('runoob'); 
  // true 
   
  site.includes('baidu'); 
  // false
  ```

  

####  indexOf()

##### indexOf: function indexOf()	 搜索数组中的元素，并返回它所在的位置。

- ###### 语法

  ```
  array.indexOf(item,start)
  
  indexOf() 方法可返回数组中某个指定的元素位置。
  该方法将从头到尾地检索数组，看它是否含有对应的元素。开始检索的位置在数组 start 处或数组的开头（没有指定 start 参数时）。如果找到一个 item，则返回 item 的第一次出现的位置。开始位置的索引为 0。
  如果在数组中没找到指定元素则返回 -1。
  ```

- ###### 参数

  ```
  item 	必须。查找的元素。
  start 	可选的整数参数。规定在数组中开始检索的位置。它的合法取值是 0 到 stringObject.length - 1。如省略该参数，则将从字符串的首字符开始检索。
  ```

- ###### 返回值

  ```
  Number 	元素在数组中的位置，如果没有搜索到则返回 -1。
  ```

- ###### 实例

  ```
  查找数组中的 "Apple" 元素：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  var a = fruits.indexOf("Apple");
  
  a 结果输出：
  2
  以上输出结果意味着 "Apple" 元素位于数组中的第 3 个位置。
  ```

  

#### isArray()

##### isArray() :判断对象是否为数组。

- ###### 语法

  ```
  Array.isArray(obj)
  
  isArray() 方法用于判断一个对象是否为数组。
  如果对象是数组返回 true，否则返回 false。
  ```

- ###### 参数

  ```
  obj 	必需，要判断的对象。
  ```

- ###### 返回值

  ```
  布尔值，如果对象是数组返回 true，否则返回 false。
  ```

- ###### 实例

  ```
  判断对象是否为数组：
  function myFunction() {
      var fruits = ["Banana", "Orange", "Apple", "Mango"];
      var x = document.getElementById("demo");
      x.innerHTML = Array.isArray(fruits);
  }
  
  ```

  

#### join()	

##### join: function join()	 	把数组的所有元素放入一个字符串。

- ###### 语法

  ```
  array.join(separator)
  
  join() 方法用于把数组中的所有元素转换一个字符串。
  元素是通过指定的分隔符进行分隔的。
  ```

- ###### 参数

  ```
  separator 	可选。指定要使用的分隔符。如果省略该参数，则使用逗号作为分隔符。
  ```

- ###### 返回值

  ```
  String 	返回一个字符串。该字符串是通过把 arrayObject 的每个元素转换为字符串，然后把这些字符串连接起来，在两个元素之间插入 separator 字符串而生成的。
  ```

- ###### 实例

  ```
  把数组中的所有元素转换为一个字符串：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  var energy = fruits.join();
  
  energy输出结果：
  Banana,Orange,Apple,Mango 
  ```

  

#### keys()	

##### keys: function keys()	返回数组的可迭代对象，包含原始数组的键(key)。

- ###### 语法

  ```
  array.keys()
  keys() 方法用于从数组创建一个包含数组键的可迭代对象。
  如果对象是数组返回 true，否则返回 false。
  ```

- ###### 参数

  ```
  没有参数。
  ```

- ###### 返回值

  ```
  一个数组可迭代对象。
  ```

- ###### 实例

  ```
  从数组 fruit 创建一个数组迭代对象， 该对象包含了数组的键：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.keys();
  
  ```

  

#### lastIndexOf()

##### lastIndexOf: function lastIndexOf()	搜索数组中的元素，并返回它最后出现的位置。

- ###### 语法

  ```
  array.lastIndexOf(item,start)
  
  lastIndexOf() 方法可返回一个指定的元素在数组中最后出现的位置，从该字符串的后面向前查找。
  如果要检索的元素没有出现，则该方法返回 -1。
  该方法将从尾到头地检索数组中指定元素 item。开始检索的位置在数组的 start 处或数组的结尾（没有指定 start 参数时）。如果找到一个 item，则返回 item 从尾向前检索第一个次出现在数组的位置。数组的索引开始位置是从 0 开始的。
  如果在数组中没找到指定元素则返回 -1。
  ```

- ###### 参数

  ```
  item 	必需。规定需检索的字符串值。
  start 	可选的整数参数。规定在字符串中开始检索的位置。它的合法取值是 0 到 stringObject.length - 1。如省略该参数，则将从字符串的最后一个字符处开始检索。
  ```

- ###### 返回值

  ```
  Number 	如果在 stringObject 中的 fromindex 位置之前存在 searchvalue，则返回的是出现的最后一个 searchvalue 的位置。
  ```

- ###### 实例

  ```
  查找数组元素 "Apple"出现的位置：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  var a = fruits.lastIndexOf("Apple");
  
  a 输出结果：
  2
  
  以上实例输出结果意味着 "Apple" 位于数组中的第 2 个位置.
  ```

  

#### map()

##### map: function map()		通过指定函数处理数组的每个元素，并返回处理后的数组。

- ###### 语法

  ```
  array.map(function(currentValue,index,arr), thisValue)
  
  map() 方法返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值。
  map() 方法按照原始数组元素顺序依次处理元素。
  注意： map() 不会对空数组进行检测。
  注意： map() 不会改变原始数组。
  ```

- ###### 参数

  ```
  currentValue 	必须。当前元素的值
  index 	可选。当前元素的索引值
  arr 	可选。当前元素属于的数组对象
  thisValue 	可选。对象作为该执行回调时使用，传递给函数，用作 "this" 的值。
  如果省略了 thisValue，或者传入 null、undefined，那么回调函数的 this 为全局对象。
  ```

- ###### 返回值

  ```
  返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值。
  ```

- ###### 实例

  ```
  返回一个数组，数组中元素为原始数组的平方根:
  var numbers = [4, 9, 16, 25];
  
  function myFunction() {
      x = document.getElementById("demo")
      x.innerHTML = numbers.map(Math.sqrt);
  }
  
  输出结果为:
  2,3,4,5
  ```

  

#### pop()	

##### pop: function pop()	删除数组的最后一个元素并返回删除的元素。

- ###### 语法

  ```
  array.pop()
  
  pop() 方法用于删除数组的最后一个元素并返回删除的元素。
  注意：此方法改变数组的长度！
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  所有类型* 	The removed array item
  ```

- ###### 实例

  ```
  移除最后一个数组元素
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.pop();
  
  fruits 结果输出：
  Banana,Orange,Apple
  ```

  

####  push()

##### push: function push()	向数组的末尾添加一个或更多元素，并返回新的长度。

- ###### 语法

  ```
  array.push(item1, item2, ..., itemX)
  
  push() 方法可向数组的末尾添加一个或多个元素，并返回新的长度。
  注意： 新元素将添加在数组的末尾。
  注意： 此方法改变数组的长度。
  提示： 在数组起始位置添加元素请使用 unshift() 方法。
  ```

- ###### 参数

  ```
  item1, item2, ..., itemX 	必需。要添加到数组的元素。
  ```

- ###### 返回值

  ```
  Number 	数组新长度
  ```

- ###### 实例

  ```
  添加一个以上元素
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.push("Kiwi","Lemon","Pineapple")
  
  以上实例将输出
  Banana,Orange,Apple,Mango,Kiwi,Lemon,Pineapple
  ```

  

#### reduce()	

##### reduce: function reduce()	将数组元素计算为一个值（从左到右）。

- ###### 语法

  ```
  array.reduce(function(total, currentValue, currentIndex, arr), initialValue)
  
  reduce() 方法接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值。
  reduce() 可以作为一个高阶函数，用于函数的 compose。
  注意: reduce() 对于空数组是不会执行回调函数的。
  ```

- ###### 参数

  ```
  total 	必需。初始值, 或者计算结束后的返回值。
  currentValue 	必需。当前元素
  currentIndex 	可选。当前元素的索引
  arr 	可选。当前元素所属的数组对象。
  initialValue 	可选。传递给函数的初始值
  ```

- ###### 返回值

  ```
  返回计算结果
  ```

- ###### 实例

  ```
  计算数组元素相加后的总和：
  var numbers = [65, 44, 12, 4];
   
  function getSum(total, num) {
      return total + num;
  }
  function myFunction(item) {
      document.getElementById("demo").innerHTML = numbers.reduce(getSum);
  }
  
  输出结果：
  125 
  ```

  

#### reduceRight()

##### reduceRight: function reduceRight()	将数组元素计算为一个值（从右到左）。

- ###### 语法

  ```
  array.reduceRight(function(total, currentValue, currentIndex, arr), initialValue)
  
  reduceRight() 方法的功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前将数组中的数组项做累加。
  注意: reduce() 对于空数组是不会执行回调函数的。
  ```

- ###### 参数

  ```
  total 	必需。初始值, 或者计算结束后的返回值。
  currentValue 	必需。当前元素
  currentIndex 	可选。当前元素的索引
  arr 	可选。当前元素所属的数组对象。
  initialValue 	可选。传递给函数的初始值
  ```

- ###### 返回值

  ```
  返回计算结果
  ```

- ###### 实例

  ```
  计算数组元素相加后的总和：
  var numbers = [65, 44, 12, 4];
   
  function getSum(total, num) {
      return total + num;
  }
  function myFunction(item) {
      document.getElementById("demo").innerHTML = numbers.reduceRight(getSum);
  }
  
  输出结果：
  125 
  ```

  

#### reverse()

##### reverse: function reverse()	 	反转数组的元素顺序。

- ###### 语法

  ```
  array.reverse()
  
  reverse() 方法用于颠倒数组中元素的顺序。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  Array 	颠倒顺序后的数组
  ```

- ###### 实例

  ```
  颠倒数组中元素的顺序：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.reverse();
  
  fruits 结果输出：
  Mango,Apple,Orange,Banana
  ```

  

#### shift()

##### shift: function shift()	删除并返回数组的第一个元素。

- ###### 语法

  ```
  array.shift()
  
  shift() 方法用于把数组的第一个元素从其中删除，并返回第一个元素的值。
  注意： 此方法改变数组的长度！
  提示: 移除数组末尾的元素可以使用 pop() 方法。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  任何类型（*） 	数组原来的第一个元素的值（移除的元素）。
  ```

- ###### 实例

  ```
  从数组中移除元素:
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.shift()
  
  fruits结果输出:
  Orange,Apple,Mango 
  ```

  

#### slice()

##### slice: function slice()	选取数组的的一部分，并返回一个新数组。

- ###### 语法

  ```
  array.slice(start, end)
  
  slice() 方法可从已有的数组中返回选定的元素。
  slice()方法可提取字符串的某个部分，并以新的字符串返回被提取的部分。
  注意： slice() 方法不会改变原始数组。
  ```

- ###### 参数

  ```
  start 	可选。规定从何处开始选取。如果是负数，那么它规定从数组尾部开始算起的位置。也就是说，-1 指最后一个元素，-2 指倒数第二个元素，以此类推。
  end 	可选。规定从何处结束选取。该参数是数组片断结束处的数组下标。如果没有指定该参数，那么切分的数组包含从 start 到数组结束的所有元素。如果这个参数是负数，那么它规定的是从数组尾部开始算起的元素。
  ```

- ###### 返回值

  ```
  Array 	返回一个新的数组，包含从 start 到 end （不包括该元素）的 arrayObject 中的元素。
  ```

- ###### 实例

  ```
  在数组中读取元素：
  var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
  var citrus = fruits.slice(1,3);
  
  citrus 结果输出:
  Orange,Lemon
  ```

  

####  some()	

##### some: function some()	 	检测数组元素中是否有元素符合指定条件。

- ###### 语法

  ```
  array.some(function(currentValue,index,arr),thisValue)
  
  some() 方法用于检测数组中的元素是否满足指定条件（函数提供）。
  some() 方法会依次执行数组的每个元素：
      如果有一个元素满足条件，则表达式返回true , 剩余的元素不会再执行检测。
      如果没有满足条件的元素，则返回false。
  注意： some() 不会对空数组进行检测。
  注意： some() 不会改变原始数组。
  ```

- ###### 参数

  ```
  currentValue 	必须。当前元素的值
  index 	可选。当前元素的索引值
  arr 	可选。当前元素属于的数组对象
  thisValue 	可选。对象作为该执行回调时使用，传递给函数，用作 "this" 的值。
  如果省略了 thisValue ，"this" 的值为 "undefined"
  ```

- ###### 返回值

  ```
   	布尔值。如果数组中有元素满足条件返回 true，否则返回 false。
  ```

- ###### 实例

  ```
  检测数组中是否有元素大于 18:
  var ages = [3, 10, 18, 20];
  
  function checkAdult(age) {
      return age >= 18;
  }
  
  function myFunction() {
      document.getElementById("demo").innerHTML = ages.some(checkAdult);
  }
  
  输出结果为:
  true
  ```

  

#### sort()

##### sort: function sort()	 	对数组的元素进行排序。

- ###### 语法

  ```
  array.sort(sortfunction)
  
  sort() 方法用于对数组的元素进行排序。
  排序顺序可以是字母或数字，并按升序或降序。
  默认排序顺序为按字母升序。
  注意：当数字是按字母顺序排列时"40"将排在"5"前面。
  使用数字排序，你必须通过一个函数作为参数来调用。
  函数指定数字是按照升序还是降序排列。
  这些说起来可能很难理解，你可以通过本页底部实例进一步了解它。
  
  注意： 这种方法会改变原始数组！。
  ```

- ###### 参数

  ```
  sortfunction 	可选。规定排序顺序。必须是函数。
  ```

- ###### 返回值

  ```
  Array 	对数组的引用。请注意，数组在原数组上进行排序，不生成副本。
  ```

- ###### 实例

  ```
  数组排序：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.sort();
  
  fruits 输出结果：
  Apple,Banana,Mango,Orange
  ```

  

#### splice()	

##### splice: function splice()	 	从数组中添加或删除元素。

- ###### 语法

  ```
  array.splice(index,howmany,item1,.....,itemX)
  
  splice() 方法用于添加或删除数组中的元素。
  注意：这种方法会改变原始数组。
  ```

- ###### 参数

  ```
  index 	必需。规定从何处添加/删除元素。
  该参数是开始插入和（或）删除的数组元素的下标，必须是数字。
  howmany 	可选。规定应该删除多少元素。必须是数字，但可以是 "0"。
  如果未规定此参数，则删除从 index 开始到原数组结尾的所有元素。
  item1, ..., itemX 	可选。要添加到数组的新元素
  ```

- ###### 返回值

  ```
  Array 	如果从 arrayObject 中删除了元素，则返回的是含有被删除的元素的数组。
  ```

- ###### 实例

  ```
  数组中添加新元素：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.splice(2,0,"Lemon","Kiwi");
  
  fruits 输出结果：
  Banana,Orange,Lemon,Kiwi,Apple,Mango
  ```

  

#### toLocaleString()	 

##### toLocaleString: function toLocaleString()	 方法可根据本地时间把 Date 对象转换为字符串，并返回结果。

- ###### 语法

  ```
  dateObject.toLocaleString()
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  dateObject 的字符串表示，以本地时间区表示，并根据本地规则格式化。
  ```

- ###### 实例

  ```
  在本例中，我们将根据本地时间把今天的日期转换为字符串：
  
  <script type="text/javascript">
  var d = new Date()
  document.write(d.toLocaleString())
  </script>
  
  输出：
  2019/9/10 下午11:48:36
  ```

  

#### toSource()

##### toSource: function toSource() 表示对象的源代码。

- ###### 语法

  ```
  object.toSource()
  
  toSource() 方法表示对象的源代码。
  该原始值由 Array 对象派生的所有对象继承。
  toSource() 方法通常由 JavaScript 在后台自动调用，并不显式地出现在代码中。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  
  ```

- ###### 实例

  ```
  <script type="text/javascript">
  
  function employee(name,job,born)
  {
  this.name=name;
  this.job=job;
  this.born=born;
  }
  
  var bill=new employee("Bill Gates","Engineer",1985);
  
  document.write(bill.toSource());
  
  </script>
  
  输出：
  
  ({name:"Bill Gates", job:"Engineer", born:1985}) 
  ```

  

#### toString()

##### toString: function toString()	把数组转换为字符串，并返回结果。

- ###### 语法

  ```
  array.toString()
  
  toString() 方法可把数组转换为字符串，并返回结果。
  注意： 数组中的元素之间用逗号分隔。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  String 	数组的所有值用逗号隔开
  ```

- ###### 实例

  ```
  将数组转换为字符串：
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.toString();
  
  fruits将输出：
  Banana,Orange,Apple,Mango
  ```

  

#### unshift() 

##### unshift: function unshift()  	向数组的开头添加一个或更多元素，并返回新的长度。

- ###### 语法

  ```
  array.unshift(item1,item2, ..., itemX)
  
  unshift() 方法可向数组的开头添加一个或更多元素，并返回新的长度。
  注意： 该方法将改变数组的数目。
  提示: 将新项添加到数组末尾，请使用 push() 方法。
  ```

- ###### 参数

  ```
  item1,item2, ..., itemX 	可选。向数组起始位置添加一个或者多个元素。
  ```

- ###### 返回值

  ```
  Type 描述 Number 数组新长度 
  ```

- ###### 实例

  ```
  将新项添加到数组起始位置:
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  fruits.unshift("Lemon","Pineapple");
  
  fruits 将输出：
  Lemon,Pineapple,Banana,Orange,Apple,Mango
  ```

  

#### values()

##### values: function values()	它会返回一个对象，包含指定数组的元素值。

- ###### 语法

  ```
  arr.values()
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  一个遍历器对象
  ```

- ###### 实例

  ```
  let arr = ["蚂蚁部落", "www.softwhy.com", 4, "antzone"];
  var iterator = arr.values();
  for (let elem of iterator) {
    console.log(elem);
  }
  
  www.softwhy.com
  4
  antzone
  ```

  

#### valueOf()

##### valueOf():	 	返回数组对象的原始值。

- ###### 语法

  ```
  array.valueOf()
  
  valueOf() 方法返回 Array 对象的原始值。
  该原始值由 Array 对象派生的所有对象继承。
  valueOf() 方法通常由 JavaScript 在后台自动调用，并不显式地出现在代码中。
  注意： valueOf() 方法不会改变原数组。
  ```

- ###### 参数

  ```
  无
  ```

- ###### 返回值

  ```
  Array 	valueOf() 返回数组值
  ```

- ###### 实例

  ```
  valueOf() 是数组对象的默认方法。
  var fruits = ["Banana", "Orange", "Apple", "Mango"];
  var v=fruits.valueOf();
  
   fruits.valueOf()与 fruits返回值一样。
  
  v输出结果为：
  Banana,Orange,Apple,Mango
  ```

  

#### values()

##### Symbol(Symbol.iterator): function values()

- ###### 语法

  ```
  
  ```

- ###### 参数

  ```
  
  ```

- ###### 返回值

  ```
  
  ```

- ###### 实例

  ```
  
  ```

  

#### xx

##### Symbol(Symbol.unscopables): Object { copyWithin: true, entries: true, fill: true, … }

- ###### 语法

  ```
  
  ```

- ###### 参数

  ```
  
  ```

- ###### 返回值

  ```
  
  ```

- ###### 实例

  ```
  
  ```

  

