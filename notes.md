#数组的方法
### concat
##### 用法
- 用于连接两个或多个数组；不改变现有数据，而是返回被连接数组的一个副本
#####例：
```
var a = [1, 2];
var b = [3, 4, 5];
var c = [6];
var d = a.concat(b,c);
```
#####输出结果
```
[1, 2, 3, 4, 5, 6]
```
### constructor
##### 用法
- 返回对象的构造函数
#####例
```
var test=new Array();
if (test.constructor==Array)
{
    document.write("This is an Array");
}
    if (test.constructor==Boolean)
{
    document.write("This is a Boolean");
}
    if (test.constructor==Date)
{
     document.write("This is a Date");
}
     if (test.constructor==String)
{
     document.write("This is a String");
}
```
#####输出结果
``
This is an Array
``
### copyWithin
##### 用法
- 用于从数组的指定位置拷贝元素到数组的另一个指定位置中
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.copyWithin(2, 0);
console.log(fruits)
```
#####输出结果
```
(4) ["Banana", "Orange", "Banana", "Orange"]
```
### entries
##### 用法
- 返回一个数组的迭代对象，该对象包含数组的键值对 (key/value)。 

  迭代对象中数组的索引值作为 key， 数组元素作为 value。
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.entries();
console.log(fruits)
```
#####输出结果
```
(4) ["Banana", "Orange", "Apple", "Mango"]
0: "Banana"
1: "Orange"
2: "Apple"
3: "Mango"
```
### every
##### 用法
- every() 方法用于检测数组所有元素是否都符合指定条件（通过函数提供）。
  
  every() 方法使用指定函数检测数组中的所有元素：
  
  如果数组中检测到有一个元素不满足，则整个表达式返回 false ，且剩余的元素不会再进行检测。
  
  如果所有元素都满足条件，则返回 true。
  
  注意： every() 不会对空数组进行检测。
  
  注意： every() 不会改变原始数组。
#####例：
```html

```
### fill
##### 用法
- 用于将一个固定值替换数组的元素
#####例：
```html

```
### filter
##### 用法
- 创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
  
  注意： filter() 不会对空数组进行检测。
  
  注意： filter() 不会改变原始数组。
#####例：
```html

```
### find
##### 用法
- find() 方法返回通过测试（函数内判断）的数组的第一个元素的值。
  
  find() 方法为数组中的每个元素都调用一次函数执行：
  
  当数组中的元素在测试条件时返回 true 时, find() 返回符合条件的元素，之后的值不会再调用执行函数。
  
  如果没有符合条件的元素返回 undefined
  
  注意: find() 对于空数组，函数是不会执行的。
  
  注意: find() 并没有改变数组的原始值。
#####例：
```html

```
### findIndex
##### 用法
- findIndex() 方法返回传入一个测试条件（函数）符合条件的数组第一个元素位置。
  
  findIndex() 方法为数组中的每个元素都调用一次函数执行：
  
  当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
  
  如果没有符合条件的元素返回 -1
  
  注意: findIndex() 对于空数组，函数是不会执行的。
  
  注意: findIndex() 并没有改变数组的原始值。
#####例：
```html

```
### flat
##### 用法
- 数组降维
#####例：
```
var arr = [1, 2, [3, 4]];
arr.flat();
```
#####输出结果
```
[1, 2, 3, 4]
```
### flatMap
##### 用法
- 用于将输入数组元素展平为新数组
#####例：
```html

```
### forEach
##### 用法
- 用于调用数组的每个元素，并将元素传递给回调函数。
  
  注意: forEach() 对于空数组是不会执行回调函数的。
#####例：
```html

```
### includes
##### 用法
- 用来判断一个数组是否包含一个指定的值，如果是返回 true，否则false。
#####例：
```html

```
### indexOf
##### 用法
- 可返回数组中某个指定的元素位置
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var a = fruits.indexOf("Apple");
```
#####输出结果
```
2
```
### join
##### 用法
- 用于把数组中的所有元素转换一个字符串
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var energy = fruits.join();
```
#####输出结果
```
Banana,Orange,Apple,Mango
```
### keys
##### 用法
- 用于从数组创建一个包含数组键的可迭代对象。
  
  如果对象是数组返回 true，否则返回 false。
#####例：
```html

```
### lastIndexOf
##### 用法
- 返回一个指定的元素在数组中最后出现的位置，从该字符串的后面向前查找。
#####例：
```html

```
### map
##### 用法
- map() 方法返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值。
  
  map() 方法按照原始数组元素顺序依次处理元素。
  
  注意： map() 不会对空数组进行检测。
  
  注意： map() 不会改变原始数组。
#####例：
```html

```
### pop
##### 用法
- 用于删除数组的最后一个元素
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();
```
#####输出结果
```
Banana,Orange,Apple
```
### push
##### 用法
- 可向数组的末尾添加一个或多个元素，并返回新的长度
#####例：
```html

```
### reduce
##### 用法
-  方法接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值。
#####例：
```
   var numbers = [65, 44, 12, 4];

   function getSum(total, num) {
       return total + num;
   }
   document.write(numbers.reduce(getSum))
```
#####输出结果
```
125
```
### reduceRight
##### 用法
- 功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前将数组中的数组项做累加
#####例：
```
   var numbers = [65, 44, 12, 4];

   function getSum(total, num) {
       return total + num;
   }
   document.write(numbers.reduceRight(getSum))
```
#####输出结果
```
125
```
### reverse
##### 用法
- 用于颠倒数组中元素的顺序
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.reverse();
```
#####输出结果
```
Mango,Apple,Orange,Banana
```
### shift
##### 用法
- 用于把数组的第一个元素从其中删除
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift()
```
#####输出结果
```
Orange,Apple,Mango
```
### slice
##### 用法
- slice() 方法可从已有的数组中返回选定的元素。
  
  slice()方法可提取字符串的某个部分，并以新的字符串返回被提取的部分。
  
  注意： slice() 方法不会改变原始数组。
#####例：
```
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1,3);
```
#####输出结果
```
Orange,Lemon
```
### some
##### 用法
- some() 方法用于检测数组中的元素是否满足指定条件（函数提供）。
  
  some() 方法会依次执行数组的每个元素：
  
  如果有一个元素满足条件，则表达式返回true , 剩余的元素不会再执行检测。
  如果没有满足条件的元素，则返回false。
  注意： some() 不会对空数组进行检测。
  
  注意： some() 不会改变原始数组。
#####例：
```
var ages = [3, 10, 18, 20];

function checkAdult(age) {
    return age >= 18;
}
document.write(ages.some(checkAdult))
```
#####输出结果
```
trye
```
### sort
##### 用法
- sort() 方法用于对数组的元素进行排序。
  
  排序顺序可以是字母或数字，并按升序或降序。
  
  默认排序顺序为按字母升序。
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
```
#####输出结果
```
Apple,Banana,Mango,Orange
```
### splice
##### 用法
- splice() 方法用于添加或删除数组中的元素。
  
  注意：这种方法会改变原始数组。
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2,0,"Lemon","Kiwi");
```
#####输出结果
```
Banana,Orange,Lemon,Kiwi,Apple,Mango
```
### toLocaleString
##### 用法
- 怎么用
#####例：
```html

```
### toString
##### 用法
- toString() 方法可把数组转换为字符串，并返回结果。
  
  注意： 数组中的元素之间用逗号分隔。
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.toString();
```
#####输出结果
```
Banana,Orange,Apple,Mango
```
### unshift
##### 用法
- 向数组的开头添加一个或更多元素
#####例：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon","Pineapple");
```
#####输出结果
```
Lemon,Pineapple,Banana,Orange,Apple,Mango
```
### values
##### 用法
- 怎么用
#####例：
```

```
#####输出结果
```

```
### Symbol(Symbol.iterator)
##### 用法
- 怎么用
#####例：
```html

```
#####输出结果
```

```
### Symbol(Symbol.unscopables)
##### 用法
- 怎么用
#####例：
```

```
#####输出结果
```

```
