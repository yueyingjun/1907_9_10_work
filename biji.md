# 数组

## push 在数组的最后追加元素

```
var arr1 = [1，2，3];
var arr2 = arr.push(4，5);
// arr1=[1,2,3,4,5]

```

## length 数组长度
```
var arr[1,2,3]
console.log(arr.length)
//3
```

## concat 合并两个或多个数组
```
var arr1[1,2,3]
var arr2[4,5,6]
var arr3[7,8,9]
var arr4 = arr1.concat(arr2,arr3)
//arr4=[1,2,3,4,5,6,7,8,9]
```

'
## copyWithin 在当前数组内部，将指定位置的成员复制到其他位置（会覆盖原有成员），然后返回当前数组。也就是说，使用这个方法，会修改当前数组

- 它接受三个参数。
  target （必需）：从该位置开始替换数据。
  start （可选）：从该位置开始读取数据，默认为 0 。如果为负值，表示倒数。
  end （可选）：到该位置前停止读取数据，默认等于数组长度。如果为负值，表示倒数。
```
var arr=[1, 2, 3, 4, 5].copyWithin(0, 3, 4)  
//arr=[4, 2, 3, 4, 5]  

```
## entries 从数组 arr创建一个可迭代对象， 该对象包含了数组的键值对：
```
var arr = ["a", "b, "c", "d"];
arr.entries();
0,a

1,b

2,c

3,d
```
## every 将所有元素进行判断返回一个布尔值，如果所有元素都满足判断条件，则返回true，否则为false：
```
var arr = [1, 2, 3, 4, 5]
    const isLessThan4 => value => value < 4
    const isLessThan6 => value => value < 6
    arr.every(isLessThan4 ) //false
    arr.every(isLessThan6 ) //true
```
## fill 使用固定值填充数组：
```
var arr = [1, 2, 3, 4];
arr.fill(5);
//arr=[5,5,5,5]

```
## filter 将所有元素进行判断，将满足条件的元素作为一个新的数组返回
```
var ages = [32, 33, 16, 40];

function checkAdult(age)  {
    return age >= 18;
}

function myFunction() {
    document.getElementById("demo").innerHTML = ages.filter(checkAdult);
}

//32 33 40

```
## find方法返回通过测试（函数内判断）的数组的第一个元素的值。
```
var arr = [3, 10, 18, 20];
 
function checkAdult(age) {
    return age >= 18;
}
 
function myFunction() {
    document.getElementById("demo").innerHTML = ages.find(checkAdult);
}
fruits 输出结果：

18
```
## findIndex方法返回传入一个测试条件（函数）符合条件的数组第一个元素位置。
```
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
## includes检测数组 是否包含 查找内容 :
```
var arr = ['a', 'b', 'c'];
 
arr.includes('a'); 
// true 
 
arr.includes('e'); 
// false

```
## indexOf查找数组中的 "b" 元素：
```
var arr = ["a", "b", "c", "d"];
var a = arr.indexOf("b");
结果输出：

1
```
## join把数组的所有元素放入一个字符串。元素通过指定的分隔符进行分隔。
```
   var arr = [1, 2, 3, 4, 5];
   var str1 = arr.toString()
   var str2 = arr.toString(',')
   var str3 = arr.toString('|')
   console.log(str1)// 12345
   console.log(str2)// 1,2,3,4,5
   console.log(str3)// 1|2|3|4|5
```
## keys用于从数组创建一个包含数组键的可迭代对象。如果对象是数组返回 true，否则返回 false。
```
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.keys();
```
## lastIndexOf可返回一个指定的元素在数组中最后出现的位置，从该字符串的后面向前查找。
```
var fruits = ["a", "b", "c", "d"];
var a = fruits.lastIndexOf("b");
a输出结果：

1
```
## map将数组中的每个元素调用一个提供的函数，结果作为一个新的数组返回，并没有改变原来的数组
```
var arr = [1, 2, 3, 4, 5]
    var newArr = arr.map(x => x*2)
    //arr= [1, 2, 3, 4, 5]   原数组保持不变
    //newArr = [2, 4, 6, 8, 10] 返回新数组
```
## pop在数组后面删除最后一个元素，并返回数组，此方法改变了数组的长度：
```
var arr = [1, 2, 3, 4, 5]
    arr.pop()
    console.log(arr) //[1, 2, 3, 4]
    console.log(arr.length) //4
```
## reduce所有元素调用返回函数，返回值为最后结果,传入的值必须是函数类型：
```
let arr = [1, 2, 3, 4, 5]
   const add = (a, b) => a + b
   let sum = arr.reduce(add)
   //sum = 15  相当于累加的效果
```


## reverse颠倒数组中元素的顺序

```
var arr = new Array(3)
arr[0] = "a"
arr[1] = "b"
arr[2] = "c"

document.write(arr + "<br />")
document.write(arr.reverse())

a,b,c
c,b,a

```
## shift在数组后面删除第一个元素，并返回数组，此方法改变了数组的长度：
```
var arr = [1, 2, 3, 4, 5]
    arr.shift()
    console.log(arr) //[2, 3, 4, 5]
    console.log(arr.length) //4 
```
## slice从某个已有的数组返回选定的元素
```
var arr = new Array(3)
arr[0] = "a"
arr[1] = "b"
arr[2] = "c"

document.write(arr + "<br />")
document.write(arr.slice(1) + "<br />")
document.write(arr)

a,b,c
b,c
a,b,c
```
## some所有元素进行判断返回一个布尔值，如果存在元素满足判断条件，则返回true，若所有元素都不满足判断条件，则返回false：
```
var arr= [1, 2, 3, 4, 5]
    const isLessThan4 => value => value < 4
    const isLessThan6 => value => value > 6
    arr.some(isLessThan4 ) //true
    arr.some(isLessThan6 ) //false
```
## sort对数组的元素进行排序
```
var arr=[5,7,1,4,2]
 arr.sort(arr);
 //1,2,4,5,7
```
## splice删除元素，并向数组添加新元素。万能方法，可以实现增删改：
```
var arr = [1, 2, 3, 4, 5];
     var arr1 = arr.splice(2, 0 'haha')
     var arr2 = arr.splice(2, 3)
     var arr1 = arr.splice(2, 1 'haha')
     console.log(arr1) //[1, 2, 'haha', 3, 4, 5]新增一个元素
     console.log(arr2) //[1, 2] 删除三个元素
     console.log(arr3) //[1, 2, 'haha', 4, 5] 替换一个元素
```
## toLocaleString把数组转换为本地数组，并返回结果。
```
var arr = new Array(3)
arr[0] = "a"
arr[1] = "b"
arr[2] = "c"

document.write(arr.toLocaleString())

a, b, c
```
## toString把数组转换为字符串，并返回结果。
```
var arr = [1, 2, 3, 4, 5];
   var str = arr.toString()
   console.log(str)
   // 1,2,3,4,5
```
## unshift将一个或多个元素添加到数组的开头，并返回新数组的长度
```
var arr = [1, 2, 3, 4, 5]
    arr.unshift(6, 7)
    console.log(arr) //[6, 7, 1, 2, 3, 4, 5]
    console.log(arr.length) //7 
```


