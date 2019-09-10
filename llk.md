#数组

#map
##1.将数组中的每个元素调用一个提供的函数，结果作为一个新的数组返回，并没有改变原来的数组
```var arr = [1,2,3,4,5]
var newArr = arr.map(x = x*2)
// arr= [1,2,3,4,5]
// newArr= [2,3,6,8,10]
```
##2.forEach将数组中的每个元素的执行传进提供的函数，没有返回值，直接改变原数组
```var arr = [1,2,3,4,5]
num.forEach(x = x*2)
// arr= [2,4,6,8,10]
```
##3.filter将所有的元素进行判断，将满足条件的元素作为一个新的数组返回
```var arr = [1,2,3,4,5]
    var newArr = arr.filter(function (value,index) {
        return value > 1
    })
    // arr = [2,3,4,5]
```
##4.every将所有的元素进行判断返回一个布尔值，如果所有元素都满足判断条件，则返回true，否则返回false
 ```var arr2 = [1,2,3,4,5]
  var end = arr2.every(function(value,index){
      return value > 4
  })
  console.log(end)
  
  // end = false
  ```
##5.some将所有的元素判断返回一个布尔值，如果存在元素满足判断条件，则返回true，若所有的元素都不满足判断条件，则返回false
 ```var arr2 = [1,2,3,4,5]
  var end = arr2.every(function(value,index){
      return value > 4
  })
  console.log(end)
  
  // end = true
  ```
##6.reduce此方法是所有元素调用返回函数，返回值为最后结果,传入的值必须是函数类型
```var arr = [1,2,3,4,5 ]
var sum = arr.reduce(function(a,b){
   retutn a+b
})

// sum = 15 
```
##7.push此方法是在数组的后面添加新加元素
```var arr = [1,2,3]
arr,push(4)
//arr = [1,2,3,4]
```
##8.pop此方法在数组后面删除最后一个元素，并返回数组
```var arr = [1,2,3]
arr.pop()
// var = [1,2]
```
##9.shift此方法在数组前面删除第一个元素，并返回数组，此方法改变了数组的长度
```var arr = [1,2,3]
arr.shift()
// arr = [2,3]
```
##10.unshift此方法是将一个或多个元素添加到数组的开头
```var arr = [1, 2, 3, 4, 5]
    arr.unshift(6, 7)
    //[6, 7, 2, 3, 4, 5]
```
##11.siArray判断一个对象是不是数组，返回的是布尔值
```var num = 1
var flag = num.isArray()
/flag = false
```
##12.,concat此方法是一个可以将多个数组拼接成一个数组
```var arr1 = [1, 2, 3]
      arr2 = [4, 5]
  var arr = arr1.concat(arr2)
  // arr = [1,2,3,4,5]
  ```
##13.toString
```此方法将数组转化为字符串
`   var  arr = [1, 2, 3, 4, 5];
   var str = arr.toString()
   // str = 1,2,3,4,5
```
##14.join
```也是将数组转化为字符串
    var arr = [1, 2, 3, 4, 5];
   var str1 = arr.toString()
   var str2 = arr.toString(',')
   var str3 = arr.toString('##')
   console.log(str1)// 12345
   console.log(str2)// 1,2,3,4,5
   console.log(str3)// 1##2##3##4##5
 ```
　　
##15.splice(开始的位置，删除的个数，元素)万能的方法，可以实现增删改
 ```  var arr = [1, 2, 3, 4, 5];
     var arr1 = arr.splice(2, 0 'haha')
     var arr2 = arr.splice(2, 3)
     var arr1 = arr.splice(2, 1 'haha')
     console.log(arr1) //[1, 2, 'haha', 3, 4, 5]新增一个元素
     console.log(arr2) //[1, 2] 删除三个元素
     console.log(arr3) //[1, 2, 'haha', 4, 5] 替换一个元素
 ```
##16.includes判断一个元素是否包含一个指定的值
 ```var arr = [1,2,3]
 var flag = arr.includes(3)
 // flag = true
 ```
##17.lastIndexOf搜索数组中的元素，并返回它最后出现的位置
 ```var arr = [2,2,4,2]
 var num = arr.lastIndexOf(2)
 // num = 3
 ```
##18.reverse反转数组的元素顺序
var arr = [1,2,3,4]
 arr.reverse();
 // arr = [4,3,2,1]

##19.sort将元素进行排序
 ```var arr = [1,3,2,6,5]
    arr.sort
    // arr = [1,2,3,5,6]
```
 
##20.slice选取数组的一部分，返回一个新的数组
```  var arr = [1,2,4,5,]
    var arr2  = arr.slice(0,2)
    // arr2= [1,2,4]
 ```
 ##21.length:计算出数组的长度。下列num就是a数组的长度
 ```
 var a=[1.2.3]
 var num=a.leng.th
 
 ```
 ##22.constructar:返回对创建此对象的数组函数的引用。text就是a的类型
 ```
 var a=new Array()
 var text=a.constructor
 
 ```
 ##23.concat:方法用于连接两个过多个数组。返回值是一个新的数组。a就是将c连接到b后的新数组
 ```
 var c=[1,2,3]
 var b=[4,5,6]
 var a=c.concat(b)
 console.log(a)
