#数组笔记
## Array.map()
- 将数组中的每个元素调用一个提供的函数，结果作为一个新的数组返回，并没有改变原来的数组
```$xslt
var arr = [1,2,3,4,5]
var newArr = arr.map(x = x*2)
// arr= [1,2,3,4,5]
// newArr= [2,3,6,8,10]
```
## Array.forEach()
- 将数组中的每个元素的执行传进提供的函数，没有返回值，直接改变原数组
```$xslt
var arr = [1,2,3,4,5]
num.forEach(x = x*2)
// arr= [2,4,6,8,10]
```
## Array.filter
- 将所有的元素进行判断，将满足条件的元素作为一个新的数组返回
```$xslt
var arr = [1,2,3,4,5]
    var newArr = arr.filter(function (value,index) {
        return value > 1
    })
    // arr = [2,3,4,5]
```
## Array.every
- 将所有的元素进行判断返回一个布尔值，如果所有元素都满足判断条件，则返回true，否则返回false
```$xslt
  var arr2 = [1,2,3,4,5]
  var end = arr2.every(function(value,index){
      return value > 4
  })
  console.log(end)
  
  // end = false
```
## Array.some
- 将所有的元素判断返回一个布尔值，如果存在元素满足判断条件，则返回true，若所有的元素都不满足判断条件，则返回false
```$xslt
 var arr2 = [1,2,3,4,5]
  var end = arr2.every(function(value,index){
      return value > 4
  })
  console.log(end)
  
  // end = true
```
## Array.reduce
- 此方法是所有元素调用返回函数，返回值为最后结果,传入的值必须是函数类型
 ```$xslt
var arr = [1,2,3,4,5 ]
var sum = arr.reduce(function(a,b){
    retutn a+b
})

// sum = 15 
```
## Array.push
-  此方法是在数组的后面添加新加元素
```$xslt
var arr = [1,2,3]
arr,push(4)
//arr = [1,2,3,4]
```

## Array.pop
- 此方法在数组后面删除最后一个元素，并返回数组
```$xslt
var arr = [1,2,3]
arr.pop()
// var = [1,2]
```
## Array,shift
-  此方法在数组前面删除第一个元素，并返回数组，此方法改变了数组的长度
```$xslt
var arr = [1,2,3]
arr.shift()
// arr = [2,3]
```
## Array,unshift
- 此方法是将一个或多个元素添加到数组的开头
```$xslt
var arr = [1, 2, 3, 4, 5]
    arr.unshift(6, 7)
    //[6, 7, 2, 3, 4, 5]
```

## Array.siArray 
- 判断一个对象是不是数组，返回的是布尔值
```$xslt
var num = 1
var flag = num.isArray()
/flag = false
```
## Array,concat
- 此方法是一个可以将多个数组拼接成一个数组
```$xslt
var arr1 = [1, 2, 3]
      arr2 = [4, 5]
  var arr = arr1.concat(arr2)
  // arr = [1,2,3,4,5]
```
## Array.toString
-  此方法将数组转化为字符串
```$xslt
`   var  arr = [1, 2, 3, 4, 5];
   var str = arr.toString()
   // str = 1,2,3,4,5
```
## Array.join
- 也是将数组转化为字符串
```$xslt
    var arr = [1, 2, 3, 4, 5];
   var str1 = arr.toString()
   var str2 = arr.toString(',')
   var str3 = arr.toString('##')
   console.log(str1)// 12345
   console.log(str2)// 1,2,3,4,5
   console.log(str3)// 1##2##3##4##5
　　
```
## Array.splice(开始的位置，删除的个数，元素)
- 万能的方法，可以实现增删改
```$xslt
     var arr = [1, 2, 3, 4, 5];
     var arr1 = arr.splice(2, 0 'haha')
     var arr2 = arr.splice(2, 3)
     var arr1 = arr.splice(2, 1 'haha')
     console.log(arr1) //[1, 2, 'haha', 3, 4, 5]新增一个元素
     console.log(arr2) //[1, 2] 删除三个元素
     console.log(arr3) //[1, 2, 'haha', 4, 5] 替换一个元素
```
## Array.includes
- 判断一个元素是否包含一个指定的值
```$xslt
 var arr = [1,2,3]
 var flag = arr.includes(3)
 // flag = true
```
## Array.lastIndexOf
-  搜索数组中的元素，并返回它最后出现的位置
```$xslt
 var arr = [2,2,4,2]
 var num = arr.lastIndexOf(2)
 // num = 3
```
## Array.reverse
- 反转数组的元素顺序
```$xslt
 var arr = [1,2,3,4]
 arr.reverse();
 // arr = [4,3,2,1]
```
## Array.sort
- 将元素进行排序
```$xslt
    var arr = [1,3,2,6,5]
    arr.sort
    // arr = [1,2,3,5,6]
```
## Arrar.slice
- 选取数组的一部分，返回一个新的数组
```$xslt
    var arr = [1,2,4,5,]
    var arr2  = arr.slice(0,2)
    // arr2= [1,2,4]
```
