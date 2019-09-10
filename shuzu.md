# 数组的方法

1..concat()  连接两个或更多的数组，并返回结果
```
var arr1=[1,2,3] arr2=[4,5]
console.log(arr1.concat(arr2))
结果：[1,2,3,4,5]
```

2..constructor  返回对创建此对象的数组函数的引用
```$xslt
var arr=new Array()
console.log(arr.constructor)
结果：Array
```

3..copyWithin   从数组的指定位置拷贝元素到数组的另一个指定位置中

* array.copyWithin(target,start,end)

- target:复制到指定索引位置
- start：元素复制的起始位置  可选
- end ：停止复制的索引位置(默认为array.length).如果为负值，表示倒数

```$xslt
var fruits = ["B","O", "A", "M", "K", "P"]
console.log(fruits.copyWithin(2, 0, 2))
结果：B,O,B,O,K,P
```
4..entries() 返回一个数组的迭代对象，该对象包含数组的键值对(key/value)

- key:索引值   value:数组元素
```$xslt
var arr=["a","b","c"]
console.log(arr.entries())
结果:[0,"a"]
     [1,"b"]
     [2,"c"]
```
5..every() 用于检测数组所有元素是否符合指定条件(通过函数)

- 如果数组中检测到有一个元素不满足，则整个表达式返回false，且剩余的元素不会在进行检测
- 如果所有的元素都满足条件，则返回true
- every()不会对空数组进行检测
- every()不会改变原始数组
```
var arr=[12,23,34,45]
arr.every(function(currentValue,index,arr),thisValue)
```
6..fill() 用于将一个固定值替换数组的元素。

- array.fill(value,start,end)
- value:填充的值，start:开始填充的位置，end：停止填充的位置
```
var arr=["a","b","c"]
console.log(arr.fill("e",2,3))
结果：["a","b","e"]
```
7..filter() 创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素

- filter()不会对空数组进行检测
- filter()不会改变原始数组
- 用法与every()类似，只不过返回值不一样，every()返回boolean值，filter返回一个新数组
```
var arr=[12,23,34,45]
arr.filter(function(currentValue,index,arr),thisValue)
```
8..find() 返回通过测试(函数内判断)的数组的第一个元素的值

- find()方法为数组中的每个元素都调用一次函数执行
   
   - 当数组中的元素在测试条件是返回true时，find()返回符合条件的元素，之后的值不会在调用执行函数
   - 如果没有符合条件的元素返回undefined
   
* 注意：find()对于空数组，函数不会执行，不改变数组的原始值
```
var arr=[12,23,34,45]
arr.find(function(currentValue,index,arr),thisValue)
```
9..findindex() 返回传入一个测试条件(函数)符合的数组的第一个元素位置(索引)

- findindex()方法为数组中的每个元素都调用一次函数执行

   - 当数组中的元素在测试条件是返回true时，findindex()返回符合条件的元素的索引位置，之后的值不会在调用执行函数
   - 如果没有符合条件的元素返回-1
   
- 注意：同上
```
var arr=[12,23,34,45]
arr.find(function(currentValue,index,arr),thisValue)
```
10..flat()会按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的子数组中的元素合并为一个新数组返回

- 语法：var arr=arr.flat([depth])    depth:指定要提取嵌套数组的结构深度，默认值为1  返回一个新数组
- flat()会移除数组中的空项
```
var arr = [1, 2, , 4, 5]
console.log(arr.flat())
结果:[1, 2, 4, 5]
```
11..flatmap()首先使用映射函数映射每个元素，然后将结果压缩成一个新数组，它与map和深度值1的flat几乎相同，但flatmap通常在合并成一种方法的效率稍微高一些

- 用法:var new_array = arr.flatMap(function callback(currentValue, index, array) {
     })
```
var arr = [1, 2, 3, 4]
arr1=arr.flatMap(x => [x * 2])
console.log(arr1)
结果:arr1=[2,4,6,8]
``` 
12..forEach()用于调用数组的每个元素，并将元素传递给回调函数

- 语法:array.forEach(function(currentValue, index, arr), thisValue)
- 注意:对于空数组是不会执行回调函数的


13..includes()用来判断一个数组是否包含一个指定的值，如果是返回true，否则false

- 语法:
   - arr.includes(searchElement)
   - arr.includes(searchElement, fromIndex)
- 注意:
  - 如果fromIndex大于等于数组长度，则返回false，该数组不会被搜索
  - 如果 fromIndex 为负值，计算出的索引将作为开始搜索searchElement的位置。如果计算出的索引小于 0，则整个数组都会被搜索
```
var arr = ['a', 'b', 'c']
console.log(arr.includes('c', 100))  //false
console.log(arr.includes('a', -100))  //true
```
14..indexOf()返回数组中某个指定的元素位置

- 用法:从头到尾地检索数组，看它是否含有对应的元素。开始检索的位置在数组 start 处或数组的开头（没有指定 start 参数时）。如果找到一个 item，则返回 item 的第一次出现的位置。开始位置的索引为 0。
     如果在数组中没找到指定元素则返回 -1。
- 语法：arr.indexOf(item,start)
```
var arr = ['a', 'b', 'c']
var a = arr.indexOf("c",2)
console.log(a)
结果:2
```
15..join()用于把数组中的所有元素转换一个字符串，元素通过制定的分隔符进行分割

- 语法:var str=arr.join(separator)  separator: 如果省略则默认用逗号
```
var arr = ['a', 'b', 'c']
var str=arr.join()
console.log(str)
结果：a,b,c
```
16..keys()从数组创建一个包含数组键的可迭代对象,如果对象是数组返回 true，否则返回 false

- 语法：arr.keys()

17..lastIndexOf()返回一个指定的元素在数组中最后出现的位置，从该字符串的后面向前查找,如果要检索的元素没有出现，则该方法返回 -1

- 用法:从尾到头地检索数组中指定元素 item。开始检索的位置在数组的 start 处或数组的结尾（没有指定 start 参数时）。如果找到一个 item，则返回 item 从尾向前检索第一个次出现在数组的位置。数组的索引开始位置是从 0 开始的。如果在数组中没找到指定元素则返回 -1
- 语法:var a=array.lastIndexOf(item,start)  start：规定在字符串中开始检索的位置，它的合法取值是0到arr.length-1，如果省略，则从字符串最后一个自符处开始
```
var arr=[1,2,3,4,1]
var a=arr.lastIndexOf(1)
console.log(a)
结果：4
```
18..map()返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值,按照原始数组元素顺序依次处理元素

- 语法:array.map(function(currentValue,index,arr), thisValue)


19..pop() 用于删除数组的最后一个元素并返回删除的元素,会改变数组的长度

```
var arr=[1,2,3,4]
console.log(arr.pop())
console.log(arr)
结果：4
      [1,2,3]
```
20..push()向数组的末尾添加一个或多个元素，并返回新的长度,会改变数组的长度

```
var arr=[1,2,3,4]
arr.push(5)
console.log(arr)
结果：[1,2,3,4,5]
```
21..reduce() 接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值,可以作为一个高阶函数，用于函数的 compos

- 语法：array.reduce(function(total, currentValue, currentIndex, arr), initialValue)
```

```
22..reduceRight() 从数组的末尾向前将数组中的数组项做累加

- 语法：array.reduceRight(function(total, currentValue, currentIndex, arr), initialValue)


23..reverse() 方法用于颠倒数组中元素的顺序

```
var arr=[1,2,3,4]
console.log(arr.reverse())
结果：[4,3,2,1]
```

24..shift()把数组的第一个元素从其中删除，并返回第一个元素的值

```
var arr=[1,2,3,4]
console.log(arr.shift())
结果：1
```
25..slice() 从已有的数组中返回选定的元素,提取字符串的某个部分，并以新的字符串返回被提取的部分

- 语法：array.slice(start, end）
   - start：如果是负数，那么它规定从数组尾部开始算起的位置    
   - end：如果没有指定该参数，那么切分的数组包含从 start 到数组结束的所有元素。如果这个参数是负数，那么它规定的是从数组尾部开始算起的元素
```
var arr=[1,2,3,4,5]
console.log(arr.slice(1,3))
结果：[2,3]
```
26..some()用于检测数组中的元素是否满足指定条件

- 用法：依次执行数组的每个元素，如果有一个元素满足条件，则表达式返回true , 剩余的元素不会再执行检测， 如果没有满足条件的元素，则返回false   
- 语法：array.some(function(currentValue,index,arr),thisValue)
   
   
27..用于对数组的元素进行排序。排序顺序可以是字母或数字，并按升序或降序,默认排序顺序为按字母升序

- 注意：使用数字排序是可能会出现“40”在“5”前面，这时需要通过调用函数来指定排列的顺序
```
var arr=[50,18,29,41,31]
arr.sort(function(a,b){
return a-b})
结果:[18, 29, 31, 41, 50]
```
28..splice() 方法用于添加或删除数组中的元素

- 语法:array.splice(index,howmany,item1,.....,itemX)
  - index :规定从何处添加/删除元素
  - howmany：规定应该删除多少元素。必须是数字，如果未规定此参数，则删除从 index 开始到原数组结尾的所有元素
```
var arr= ["B", "O", "A", "M"]
arr.splice(2,1,"L","K")
console.log(arr)
结果：["B", "O", "L", "K", "M"]
```
29..toString()可把数组转换为字符串，并返回结果
```
var arr= ["B", "O", "A", "M"]
console.log(arr.toString())
结果：B,O,A,M
```
30..unshift() 方法可向数组的开头添加一个或更多元素，并返回新的长度

```
var arr=[1,2,3]
console.log(arr.unshift(7))
结果：4
```
31..values() 返回一个对象，包含指定数组的元素值

```
var arr=[1,2,3]
var iterator=arr.values()
for(var j of iterator){
    console.log(j)
}
结果：1
      2
      3
```
32..toLocaleString() 把数组转换为本地字符串
 ```
var arr= ["B", "O", "A", "M"]
console.log(arr.toLocaleString())
结果：B,O,A,M
```