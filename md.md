#数组
##1.join 在数组的最后追加元素
### 将数组整理成字符串(跟字符串方法split()相对应)
### 用法：只接收一个参数:既分隔符
```
var arr = [1,2,3]
console.log(arr.join()); // 123
console.log(arr.join("-")); //1-2-3
console.log(arr); //[1,2,3](原数组不变)
```
##2.push 方法是对数组新增作用，新值会添加到数组最后，返回值是新的数组的长度，参数可接受任意数量。
用法：
```
var arr = ["L1","L2","L3"];
var count = arr.push("J1","S1");
console.log(count); // 5
console.log(arr); // ["L1", "L2", "L3", "J1", "J2"]
```
##3.pop() 方法是对数组进行删除，删除数组最后一位，减少数组的 length 值，然后返回移除的项。不接受参数。
用法：
```
var item = arr.pop();
console.log(item); // J2
console.log(arr); // ["L1", "L2", "L3", "J1"]
```
##4.concat()
###作用：将参数添加到原数组中。这个方法会先创建当前数组一个副本，然后将接收到的参数添加到这个副本
###的末尾，最后返回新构建的数组。在没有给 concat()方法传递参数的情况下，它只是复制当前数组并返回副本。
用法：
```
var arr = [1,3,5,7];
var arrCopy = arr.concat(9,[11,13]);
console.log(arrCopy); //[1, 3, 5, 7, 9, 11, 13]
console.log(arr); // [1, 3, 5, 7](原数组未被修改)
```
##5.constructor 返回对创建此对象的数组函数的引用
var test=new Array();
```
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
输出;This is an Array
##6.copyWithin 在当前数组内部，将指定位置的成员复制到其他位置（会覆盖原有成员），然后返回当前数组。也就是说，使用这个方法，会修改当前数组。
Array.prototype.copyWithin(target, start = 0, end = this.length)  
它接受三个参数。
target （必需）：从该位置开始替换数据。
start （可选）：从该位置开始读取数据，默认为 0 。如果为负值，表示倒数。
end （可选）：到该位置前停止读取数据，默认等于数组长度。如果为负值，表示倒数。
``````
//  将 3 号位复制到 0 号位  
[1, 2, 3, 4, 5].copyWithin(0, 3, 4)  
// [4, 2, 3, 4, 5]  
// -2 相当于 3 号位， -1 相当于 4 号位  
[1, 2, 3, 4, 5].copyWithin(0, -2, -1)  
// [4, 2, 3, 4, 5]  
//  将 3 号位复制到 0 号位  
[].copyWithin.call({length: 5, 3: 1}, 0, 3)  
// {0: 1, 3: 1, length: 5}  
//  将 2 号位到数组结束，复制到 0 号位  
var i32a = new Int32Array([1, 2, 3, 4, 5]);  
i32a.copyWithin(0, 2);  
// Int32Array [3, 4, 5, 4, 5]  
//  对于没有部署 TypedArray 的 copyWithin 方法的平台  
//  需要采用下面的写法  
[].copyWithin.call(new Int32Array([1, 2, 3, 4, 5]), 0, 3, 4);  
// Int32Array [4, 2, 3, 4, 5] 
``````
##7.entries从数组 fruit 创建一个可迭代对象， 该对象包含了数组的键值对：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.entries();
```
0,Banana

1,Orange

2,Apple
##8.every将所有元素进行判断返回一个布尔值，如果所有元素都满足判断条件，则返回true，否则为false：
let arr = [1, 2, 3, 4, 5]
```
const isLessThan4 => value => value < 4
const isLessThan6 => value => value < 6
arr.every(isLessThan4 ) //false
arr.every(isLessThan6 ) //true
```
##9.fill使用固定值填充数组：
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.fill("Runoob");
Runoob,Runoob,Runoob,Runoob
```

##10.filter将所有元素进行判断，将满足条件的元素作为一个新的数组返回
``````
let arr = [1, 2, 3, 4, 5]
    const isBigEnough => value => value >= 3
    let newArr = arr.filter(isBigEnough)
    //newNum = [3, 4, 5] 满足条件的元素返回为一个新的数组
``````
##11.find方法返回通过测试（函数内判断）的数组的第一个元素的值。
find() 方法为数组中的每个元素都调用一次函数执行：

当数组中的元素在测试条件时返回 true 时, find() 返回符合条件的元素，之后的值不会再调用执行函数。
如果没有符合条件的元素返回 undefined
注意: find() 对于空数组，函数是不会执行的。

注意: find() 并没有改变数组的原始值。

获取数组中年龄大于 18 的第一个元素
``````
var ages = [3, 10, 19, 20];
 
function checkAdult(age) {
    return age >= 18;
}

function myFunction() {
    document.getElementById("demo").innerHTML = ages.find(checkAdult);
}
fruits 输出结果：
19
``````
##12.findIndex方法返回传入一个测试条件（函数）符合条件的数组第一个元素位置。
findIndex() 方法为数组中的每个元素都调用一次函数执行：

当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
如果没有符合条件的元素返回 -1
注意: findIndex() 对于空数组，函数是不会执行的。

注意: findIndex() 并没有改变数组的原始值。


获取数组中年龄大于等于 18 的第一个元素索引位置
``````
var ages = [3, 10, 18, 20];
 
function checkAdult(age) {
    return age >= 18;
}
function myFunction() {
    document.getElementById("demo").innerHTML = ages.findIndex(checkAdult);
}
fruits 输出结果：
2
``````
##13.flat该方法可以将嵌套数组进行扁平化处理成一维数组,可以接受一个数字为展开的几层,默认为1层。如果不管嵌套多少层都展开可以传入一个Infinity。
这个方法可以将数组中数组合并，也可以将数组中的空元素剔除，生成一个新的数组
多维数组变一维数组
``````
let ary = [1, [2, [3, [4, 5]]], 6];
arr_flat = arr.flat(Infinity);
``````
##14.flatMap方法首先使用映射函数映射每个元素，然后将结果压缩成一个新数组。它与 map 和 深度值1的 flat 几乎相同，但 flatMap 通常在合并成一种方法的效率稍微高一些。
``````
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
``````
##15.forEach将数组中的每个元素执行传进提供的函数，没有返回值，直接改变原数组，注意和map方法区分
``````
let arr = [1, 2, 3, 4, 5]
   num.forEach(x => x*2)
   // arr = [2, 4, 6, 8, 10]  数组改变,注意和map区分

``````

##16.includes检测数组 site 是否包含 runoob :
let site = ['runoob', 'google', 'taobao'];
``````
site.includes('runoob'); 
// true 
 
site.includes('baidu'); 
// false
``````
##17.indexOf查找数组中的 "Banana" 元素：
``````
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var a = fruits.indexOf("Banana");
a 结果输出：

0
``````
##18.keys用于从数组创建一个包含数组键的可迭代对象。如果对象是数组返回 true，否则返回 false。
``````
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.keys();
``````
##19.lastIndexOf可返回一个指定的元素在数组中最后出现的位置，从该字符串的后面向前查找。

如果要检索的元素没有出现，则该方法返回 -1。

该方法将从尾到头地检索数组中指定元素 item。开始检索的位置在数组的 start 处或数组的结尾（没有指定 start 参数时）。如果找到一个 item，则返回 item 从尾向前检索第一个次出现在数组的位置。数组的索引开始位置是从 0 开始的。

如果在数组中没找到指定元素则返回 -1。

提示： 如果你想查找数组首次出现的位置，请使用 indexOf() 方法
``````
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var a = fruits.lastIndexOf("Apple");
a 输出结果：

2
``````
##20.map将数组中的每个元素调用一个提供的函数，结果作为一个新的数组返回，并没有改变原来的数组
``````
let arr = [1, 2, 3, 4, 5]
    let newArr = arr.map(x => x*2)
    //arr= [1, 2, 3, 4, 5]   原数组保持不变
    //newArr = [2, 4, 6, 8, 10] 返回新数组
``````
##21.reduce所有元素调用返回函数，返回值为最后结果,传入的值必须是函数类型：
``````
let arr = [1, 2, 3, 4, 5]
   const add = (a, b) => a + b
   let sum = arr.reduce(add)
   //sum = 15  相当于累加的效果
``````
   与之相对应的还有一个 Array.reduceRight() 方法，区别是这个是从右向左操作的
##22.reduceRight该方法的功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前将数组中的数组项做累加。
 reduce() 对于空数组是不会执行回调函数的。
 
 计算数组元素相加后的总和：
 ``````
 var numbers = [65, 44, 12, 4];
  
 function getSum(total, num) {
     return total + num;
 }
 function myFunction(item) {
     document.getElementById("demo").innerHTML = numbers.reduceRight(getSum);
 }
 输出结果：
 
 125
 ``````
##23.reverse颠倒数组中元素的顺序
``````
var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"

document.write(arr + "<br />")
document.write(arr.reverse())

George,John,Thomas
Thomas,John,George
``````
##24.shift在数组后面删除第一个元素，并返回数组，此方法改变了数组的长度：
``````
let arr = [1, 2, 3, 4, 5]
    arr.shift()
    console.log(arr) //[2, 3, 4, 5]
    console.log(arr.length) //4 
``````
##25.slice从某个已有的数组返回选定的元素
``````
var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"

document.write(arr + "<br />")
document.write(arr.slice(1) + "<br />")
document.write(arr)

George,John,Thomas
John,Thomas
George,John,Thomas
``````
##26.some将所有元素进行判断返回一个布尔值，如果存在元素满足判断条件，则返回true，若所有元素都不满足判断条件，则返回false：
``````
let arr= [1, 2, 3, 4, 5]
    const isLessThan4 => value => value < 4
    const isLessThan6 => value => value > 6
    arr.some(isLessThan4 ) //true
    arr.some(isLessThan6 ) //false
``````
##27.sort对数组的元素进行排序
``````
 var arr=[5,7,1,4,2]
 arr.sort(arr);//1,2,4,5,7
  arr3=["a","c","e","g","d","b","f"]
  arr3.sort()
  console.log(arr3)
  
  arr4=[1,30,20,5,7,12]
          arr4.sort(function (a,b) {
              return a-b
          })
          console.log(arr4)//1,5,7,12,20,30
``````
##28.splice删除元素，并向数组添加新元素。万能方法，可以实现增删改：Array.splice(开始位置， 删除的个数，元素)
``````
let arr = [1, 2, 3, 4, 5];
     let arr1 = arr.splice(2, 0 'haha')
     let arr2 = arr.splice(2, 3)
     let arr1 = arr.splice(2, 1 'haha')
     console.log(arr1) //[1, 2, 'haha', 3, 4, 5]新增一个元素
     console.log(arr2) //[1, 2] 删除三个元素
     console.log(arr3) //[1, 2, 'haha', 4, 5] 替换一个元素
``````
##29.toLocaleString把数组转换为本地数组，并返回结果。
``````
var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"

document.write(arr.toLocaleString())

George, John, Thomas
``````
##30.toString把数组转换为字符串，并返回结果。
``````
let arr = [1, 2, 3, 4, 5];
   let str = arr.toString()
   console.log(str)// 1,2,3,4,5 
##31.unShift将一个或多个元素添加到数组的开头，并返回新数组的长度：
let arr = [1, 2, 3, 4, 5]
    arr.unshift(6, 7)
    console.log(arr) //[6, 7,1, 2, 3, 4, 5]
    console.log(arr.length) //7
    ``````
##32.values返回数组对象的原始值
``````
const array1 = ['a', 'b', 'c'];
const iterator = array1.values();

for (const value of iterator) {
  console.log(value); // expected output: "a" "b" "c"
}

let arr = ['w', 'y', 'k', 'o', 'p'];
let eArr = arr.values();
// 您的浏览器必须支持 for..of 循环
// 以及 let —— 将变量作用域限定在 for 循环中
for (let letter of eArr) {
  console.log(letter);
}
``````






