#笔记

##数组方法

-
1.concat

合并两个数组，形成新的数组
```  var arr=[10,20,5,6,30,50]
           var arr1=[49,38,65,97,76,13,27,49,38,65];
           var newarr =arr.concat(arr1)
           console.log(newarr)
            [10, 20, 5, 6, 30, 50, 49, 38, 65, 97, 76, 13, 27, 49, 38, 65]
```


-
constructor

返回对象的构造函数
function Array(){native code}
ƒ Array() { [native code] }
```  var arr=[10,20,5,6,30,50]
           var arr1=[49,38,65,97,76,13,27,49,38,65];
           var newarr =arr.concat(arr1)
           console.log(newarr)
            [10, 20, 5, 6, 30, 50, 49, 38, 65, 97, 76, 13, 27, 49, 38, 65]
```
-
copywithin

从指定位置起拷贝指定的元素
传入三个参数  拷贝的起始索引位置  元素复制的起始位置 停止复制的
索引位置
含头不含尾  停止的索引不包含在被复制的内容中
停止复制的索引位置不写 默认数值为   数组长度-1

```     var arr4=[19,20,3,4,5,6]
             arr4.copyWithin(3)
             console.log(arr4)
                 [19, 20, 3, 19, 20, 3]
        var arr4=[19,20,3,4,5,6]
             arr4.copyWithin(2)
              console.log(arr4)
                  [19, 20, 19, 20, 3, 4]
        var arr4=[19,20,3,4,5,6]
               arr4.copyWithin(2,3,5)
               console.log(arr4)
                  [19, 20, 4, 5, 5, 6]
```
-
entries

返回一个数组迭代对象，包含了所有的键值对

keys只包含数组迭代对象了键

```        var arr4=[4,5,8,19,4,5,6,4,4]
            var i=arr4.entries()
           for(let a of i){
               console.log(a)
           }
         [0, 4]
        [1, 5]
        [2, 8]
       [3, 19]
       [4, 4]
       [5, 5]
       [6, 6]
         [7, 4]
        [8, 4]
```
-
keys

返回一个数组迭代对象，包含了所有的键

```var arr4=[4,5,8,19,4,5,6]
               var i=arr4.keys()
              for(let a of i){
                  console.log(a)
              }
              0
              1
              2
              3
              4
              5
              6
              

```
      
-
every

验证数组中元素是否符合一个条件  全部的元素满足为true 
有一个不满足就位false
返回true或者false
```                var arr4=[19,4,5,6,4,4]
                   function min(arr) {
                       return arr>4;
                   }
                   function main() {
                       console.log(arr4.every(min))
                   }
           main()
           false
           
           var arr4=[19,4,5,6,4,4]
                   function min(arr) {
                       return arr>3;
                   }
                   function main() {
                       console.log(arr4.every(min))
                   }
                   main()
            true
```
-
some

判断数组中是否存在满足条件的元素
只要存在一个即为true

```        var arr4=[4,5,8,19,4,5,6,4,4]
           function compare(arr) {
               return arr>10
           }
           function my() {
              console.log(arr4.some(compare))
           }
           my()
           ture
```
-

fill
使用固定的值替换数组中指定范围内的元素
```    var arr4=[19,"b",true,4,5,6]
   
           arr4.fill(10,0,3)
           console.log(arr4)
           [10, 10, 10, 4, 5, 6]
```
-
filter

提取出数组中满足某个条件的元素 并返回一个新的数组
```        var arr4=[19,4,5,6,4,4]
           function min(arr) {
               return arr>5;
           }
           function main() {
               console.log(arr4.filter(min))
           }
           main()
           [19, 6]
```
-
find

找到数组中符合某一条件的第一个元素

```        var arr4=[4,5,8,19,4,5,6,4,4]
           function min(arr) {
               return arr>5;
           }
           function main() {
               console.log(arr4.find(min))
           }
           main()
           8
```
-
findIndex

找到数组中符合某一条件的第一个元素对应的索引

```        var arr4=[4,5,8,19,4,5,6,4,4]
           function min(arr) {
               return arr>5;
           }
           function main() {
               console.log(arr4.findIndex(min))
           }
           main()
           2
```
-
flat

-
flatMap

-
foreach

-
includes

判断数组中是否包含指定元素
返回true或者false

```      var arr4=[4,5,8,19,4,5,6,4,4]
              console.log(arr4.includes(0))
              false
                    var arr4=[4,5,8,19,4,5,6,4,4]
                         console.log(arr4.includes(4))
                         true

```

-
indexOf

返回数组中某个元素第一次出现位置的索引
```
       var arr4=[19,4,5,6,4]
        var first=arr4.indexOf(4)
        console.log(first)
        1
```
-
join 

将数组中的元素转换成字符串，并以分隔符分隔开  不规定的话默认为
逗号

```        var arr4=[19,4,5,6,4,4,"b"]
           var first=arr4.join(";")
           console.log(first)
           19;4;5;6;4;4;b
             var arr4=[19,4,5,6,4,4,"b"]
                   var first=arr4.join()
                   console.log(first)
                   19,4,5,6,4,4,b

```


-
lastIndexOf

返回数组中某个元素最后一次出现位置的索引
```        var arr4=[19,4,5,6,4,4]
           var first=arr4.lastIndexOf(4)
           console.log(first)
           5
```
-
length

返回数组中元素的个数
```     var arr=[10,20,5,6,30,50]
        var len=arr.length
         console.log(len)
         6
         
```

-
map

-
pop

删除数组的最后一个元素，返回数组的最后一个元素  
与shift相反
```
  var arr4=[19,"b",true,4,5,6]
       var x=arr4.pop()
   console.log(x)
        console.log(arr4)
        6
        [19, "b", true, 4, 5]
```
-
push

向数组的末尾添加元素   与unshift相对

````  var arr4=[19,"b",true,4,5,6]
    
            arr4.push(19,20)
            console.log(arr4)
[19, "b", true, 4, 5, 6, 19, 20]

````

-
reduce

将数组元素从左到右计算为一个值
```        var arr4=[4,5,8,19,4,5,6,4,4]
           function sum1(a,b) {
               return a+b
           }
           function my() {
              console.log(arr4.reduce(sum1))
           }
           my()
           59
```
-
reduceRight

将数组元素从右向左计算为一个值
```      var arr4=[4,5,8,19,4,5,6,4,4]
           function sum1(a,b) {
               return a+b
           }
           function my() {
              console.log(arr4.reduceRight(sum1))
           }
           my()
           59
```
-
reverse

数组元素的顺序颠倒

```
    var arr4=[19,"b",true,4,5,6]
       console.log(arr4.reverse())
```

-
shift

删除数组的第一个元素，返回数组的第一个元素
与pop相反

```        var arr4=[19,"b",true,4,5,6]
          var x=arr4.shift()
      console.log(x)   19
      console.log(arr4)
      ["b", true, 4, 5, 6]
```
-
slice

提取数组中的选定的元素，并形成新的数组
数组.slice(开始的索引，结束的索引（不写默认到结束）)
含头不含尾

```        var arr4=[19,"b",true,4,5,6]
           var arr5 =arr4.slice(3,6)
      console.log(  arr5)
```

-
sort

对数组进行排序  默认顺序是升序   
数字排序时，需要调用一个函数来作为参数来决定升序还是降序
返回值大于0  位置互换 升序
返回值小于0   位置不变  降序
``` 
var arr3=["c","a","d","f"]
           arr3.sort()
           console.log(arr3)
           ["a", "c", "d", "f"]
var arr4=[19,20,3,4,5,6]
            arr4.sort()
            console.log(arr4)
           [19, 20, 3, 4, 5, 6]
var arr4=[19,20,3,4,5,6]
            arr4.sort(function (a,b) {
             return a-b
              })
             [3, 4, 5, 6, 19, 20]
var arr4=[19,20,3,4,5,6]
            arr4.sort(function (a,b) {
             return b-a
              })
             [20, 19, 6, 5, 4, 3]
```

-
splice
在指定位置添加或者删除元素   
用法：数组.splice（添加或删除元素的索引，删除个数，添加的元素）
```
        var arr4=[19,"b",true,4,5,6]

     arr4.splice(2,0,15)
        console.log(arr4)
```
-
toLocaleString

-
toString

把数组转换成字符串 返回字符串

```
var arr4=[19,20,3,4,5,6]
        console.log(arr4.toString())
       19,20,3,4,5,6
       
```

-
unshift

向数组的开头添加元素  与push相对

```      var arr4=[19,"b",true,4,5,6]
          arr4.unshift(19,20,15)
           console.log(arr4)
             [19, 20, 15, 19, "b", true, 4, 5, 6]
```
-
values

