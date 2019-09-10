# 函数
## 数组
- shift ：删除原数组的第一项 并返回删除元素的值，如果数组为空 返回undefined
~~~
var a =[1,2,3,]
var b = a.shift（）；//a:[2,3]b:1
~~~
- unshift:将参数添加到原数组开头，并返回数组的长度
~~~
var a=[1,2,3]
var b = a.unshift(-2,-1) //a:[-2,-1,1,2,3] b:5
~~~
- push : 将参数添加到原数组末尾，并返回数组的长度
~~~
var a = [1,2,3]
var b = a.push(4,5)   // a:[1,2,3,4,5] b:5
~~~
- pop : 删除原数组最后一项，并返回删除元素的值 
~~~
var a = [1,2,3]
var b =a.poop();   // a:[1,2] b ：3
~~~
- concat : 返回一个新数组，是将参数添加到原数组中构成的
~~~
var a = [1,2,3]
var b =  a.concat(4,5)  //a:[1,2,3] b:[1,2,3,4,5]
~~~
- reverse: 将数组反序
~~~
var a = [1,2,3]
var b =a.reverse();   // a:[3,2,1]  b:[3,2,1]
~~~
- sort : 按指定的参数对数组进行排序
 ~~~
 var a =[1,2,3]
 var b=a.sort(); //a:[3,2,1]  b:[3,2,1]
 ~~~
- slice(start,end): 返回从原数组中指定开始下标到结束下标之间的项组成的新数组
 ~~~
 var a = [1,2,3,4,5]
 var b =a.slice(2,5)  //a:[1,2,3,4,5]  b:[3,4,5]
 ~~~
- join(separator) : 将数组的元素组起一个字符串，以separator为分隔符，省略的话用默认逗号
 
 ~~~
 var a =[1,2,3,4]
 var b =a.join("|") //a:[1,2,3,4]  b: "1|2|3|4"
 ~~~
- splice  在数组的中间添加或删除一下元素
 ~~~
 var a = [1,2,3]
 var b = a.splice(1,2,8,)
 console.log(a)//[1,8,3]
 
 ~~~
- indexOf(item) : 从数组的左侧开始对应第一次开始的参数元素的下标
 ~~~
 var a=[1,2,3]
 var b = a.indexOf(2)
 console.log(b); //3
 ~~~
- lastIndexOf() 从数组的右侧开始查找对相应的
 ~~~
 var a = [1,2,3]
 var b = a.lastIndexOf(2)  // 1
 ~~~
- fill  使用一个固定的值来填充数组
 ~~~
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.fill("Runoob");/////  Runoob,Runoob,Runoob,Runoob
 ~~~
- filter  ：检测数组元素，并返回符合条件所有元素的数组
 ~~~
 var ages = [32, 33, 16, 40];
 
 function checkAdult(age) {
     return age >= 18;
 }
 function myFunction() {
     document.getElementById("demo").innerHTML = ages.filter(checkAdult);
 }
 输出结果为:  32,33,40
 ~~~
 - valueOf :返回数组对象的原始值
 ~~~
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 var v=fruits.valueOf();// Banana,Orange,Apple,Mango
 ~~~
- toString  :把数组转化为字符串，并返回结果
 ~~~
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.toString();    //  Banana,Orange,Apple,Mango
 ~~~
- map ： 通过指定函数处理数组的每个元素，返回处理后的数组
  ~~~
  var numbers = [4, 9, 16, 25];
  function myFunction() {
      x = document.getElementById("demo")
      x.innerHTML = numbers.map(Math.sqrt);
  }  //2,3,4,5
  ~~~
