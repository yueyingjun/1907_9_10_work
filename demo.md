# 数组中的方法
## 1、concat():连接两个或更多的数组，并返回结果
```
    var a[1,2,3]
    var b[4,5]
    var c=a.concat(b)
    console.log(c)
    结果是：[1,2,3,4,5]
```
## 2、copyWithin():从数组的指定位置拷贝元素到数组的另一个指定位置
      共有三个参数 target（必须有） 指定目标索引位置
                    start   元素复制的起始位置
                    end    停止辅助的索引位置，如果为负值，表示倒着数
```
    var fruits = ["Banana", "Orange", "Apple", "Mango", "Kiwi", "Papaya"];
    fruits.copyWithin(2, 0, 2);
    console.log(fruits)
    结果是：["Banana","Orange","Banana","Orange","Kiwi","Papaya"]

```
## 3、 entries（）：返回数组的可迭代对象
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.entries();
    console.log(fruits)
    结果是：["Banana","Orange","Apple","Mango"]
```
## 4、constructor（）：返回fruits数组对象原型创建的函数：
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    console.log(fruits.constructor);
    结果是：function Array() { [native code] }
```
## 5、every（）：用于检测数组所有元素是否都符合指定条件（通过函数提供）
    使用指定函数检测数组中的所有元素：
    如果数组中检测到有一个元素不满足，则整个表达式返回 false ，且剩余的元素不会再进行检测。
    如果所有元素都满足条件，则返回 true。
```
    var a = [32, 33, 16, 40];
    function abc(a) {
        return a >= 18;
    }
    console.log(a.every(abc))
    结果是:false
}
```
## 6、 fill()：用于将一个固定值替换数组的元素。
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.fill("Runoob");
    console.log(fruits)    
    结果是 ：["Runoob","Runoob",'Runoob","Runoob"
```
## 7、 filter()：创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
```
    var a = [32, 33, 16, 40];
    function abc(a) {
    return a >= 18;
    }
    var b =a.filter(abc)
    console.log(b)
    结果是：[32,33,40]
```
## 8、find()：返回通过测试（函数内判断）的数组的第一个元素的值。
    find() 方法为数组中的每个元素都调用一次函数执行：
    当数组中的元素在测试条件时返回 true 时, find() 返回符合条件的元素，之后的值不会再调用执行函数。
    如果没有符合条件的元素返回 undefined
```
    var a = [32, 33, 16, 40];
    function abc(a) {
    return a >= 18;
    }
    var b =a.find(abc)
    console.log(b)
    结果是：32
```
## 9、findIndex()：返回传入一个测试条件（函数）符合条件的数组第一个元素位置。 
    findIndex() 方法为数组中的每个元素都调用一次函数执行：
    当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
    如果没有符合条件的元素返回 -1
 ```
    var a = [32, 33, 16, 40];
    function abc(a) {
    return a >= 18;
    }
    var b =a.findIndex(abc)
    console.log(b)
    结果是：0
```   
## 10、includes():用来判断一个数组是否包含一个指定的值，如果是返回 true，否则false。
```
let site = ['runoob', 'google', 'taobao'];
site.includes('runoob'); 
// true 
site.includes('baidu'); 
// false
```
## 11、indexOf()：可返回某个指定的字符串值在字符串中首次出现的位置。如果没有找到匹配的字符串则返回 -1
注意： indexOf() 方法区分大小写。
```
    var str="Hello world, welcome to the universe.";
    var n=str.indexOf("welcome");
    console.log(n)
结果是：13
```
## 12、join() 方法用于把数组中的所有元素转换一个字符串。
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    var energy = fruits.join();
    console.log(energy)
    结果是：Banana,Orange,Apple,Mango
```
## 13、keys()：用于从数组创建一个包含数组键的可迭代对象。如果对象是数组返回 true，否则返回 false。
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    console.log(fruits.keys());
    结果是：keys() { [native code] }
```
## 14：lastIndexOf() ：可返回一个指定的字符串值最后出现的位置，如果指定第二个参数 start，则在一个字符串中的指定位置从后向前搜索。
    注意： 该方法将从后向前检索字符串，但返回是从起始位置 (0) 开始计算子字符串最后出现的位置。 看它是否含有字符串。
    开始检索的位置在字符串的 start 处或字符串的结尾（没有指定 start 时）。
    如果没有找到匹配字符串则返回 -1 。
    注意：lastIndexOf() 方法是区分大小写的！
        与indexof()类似
```
    var str="Hello world, welcome to the universe.";
    var n=str.lastIndexOf("welcome");
    console.log(n)
    结果是：13
```
## 15、length():返回数组的长度
```
var arr=[1,2,3,4,5,6,7]
console(arr.length)
结果是：7
```
## 16、map()：返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值。map() 方法按照原始数组元素顺序依次处理元素
```
    var arr=[4,9,16,25]
    console.log(arr.map(Math.sqrt))
    Math.sqrt 是对一个数进行开方处理
    结果是[2,3,4,5]
```
## 17、pop():用于删除数组的最后一个元素并返回删除的元素。
注意：此方法改变数组的长度！
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    console.log(fruits.pop());
    结果是:Mango
```
## 18、shift():用于删除数组的第一个元素并返回删除的元素。
注意：此方法改变数组的长度！
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    console.log(fruits.shift());
    结果是:Banana
```
## 19、push() :可向数组的末尾添加一个或多个元素
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.push("Kiwi")
    console.log(fruits)
    结果是：["Banana", "Orange", "Apple", "Mango", "Kiwi"]
```
## 20、unshift() :可向数组的开头添加一个或多个元素
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.unshift("Kiwi")
    console.log(fruits)
    结果是：["Kiwi", "Banana", "Orange", "Apple", "Mango"]
```
## 21、reduce():接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值。
```
var a = [65, 44, 12, 4];
function getSum(total, num) {
    return total + num;
}
var b=a.reduce(getSum)
console.log(b)
结果是：125
```
## 22、reduceRight() 方法的功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前将数组中的数组项做累加。
```
var a = [65, 44, 12, 4];
function getSum(total, num) {
    return total + num;
}
var b=a.reduceRight(getSum)
console.log(b)
结果是：125
```
## 23、reverse()：用于颠倒数组中元素的顺序。
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    console.log(fruits.reverse());
    结果是：["Mango", "Apple", "Orange", "Banana"]
```
## 24、slice()：可提取字符串的某个部分，并以新的字符串返回被提取的部分。
有两个参数：start 要抽取的片断的起始下标
            end  要截取的片段结尾的下标
```
var str="Hello world!";
var n=str.slice(1,5);
console.log(n)
结果是：ello
```
## 25、some() 方法用于检测数组中的元素是否满足指定条件（函数提供）。
some() 方法会依次执行数组的每个元素：
    如果有一个元素满足条件，则表达式返回true , 剩余的元素不会再执行检测。
    如果没有满足条件的元素，则返回false。
```
    var ages = [3, 10, 18, 20];
    function checkAdult(age) {
    return age >= 18;
    }
    console.log(ages.some(checkAdult))
    结果是：ture
```
## 26、sort() 方法用于对数组的元素进行排序。排序顺序可以是字母或数字，并按升序或降序。默认排序顺序为按字母升序。
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    console.log(fruits.sort())
    结果是：["Apple", "Banana", "Mango", "Orange"]

```
## 27、splice() 方法向/从数组中添加/删除项目，然后返回被删除的项目。
两个参数：index	必需。整数，规定添加/删除项目的位置，使用负数可从数组结尾处规定位置。
         howmany	必需。要删除的项目数量。如果设置为 0，则不会删除项目。
```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    var a=fruits.splice(2,1);
    console.log(a)
    结果是：["Apple"]
```    
## 28、toLocaleString() 方法可根据本地时间把 Date 对象转换为字符串，并返回结果。
```
var d=new Date();
var n=d.toLocaleString();
console.log(n)
结果是：2019/9/10 下午11:56:18
```
## 29、toString()：把数字转换为字符串
```
var num = 15;
var n = num.toString();
console.log(n)
结果是："15"
```
## 30、values方法获取数组的元素值
```
    var obj = { foo: 'bar', baz: 42 }
    console.log(Object.values(obj))
    结果是： ["bar", 42]
```

## 31、Symbol.iterator 为每一个对象定义了默认的迭代器
## 32、flat():会按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的字数在中的元素合并为一个新数组返回
```
var newArray=arr.flat([depth])
```
## 33、flatMap()
## 34、forEach() 方法用于调用数组的每个元素，并将元素传递给回调函数。
```
<button onclick="numbers.forEach(myFunction)">点我</button>
<p id="demo"></p>
<script>
demoP = document.getElementById("demo");
var numbers = [4, 9, 16, 25];
function myFunction(item, index) {
 demoP.innerHTML = demoP.innerHTML + "index[" + index + "]: " + item + "<br>"; 
}
输出结果：
        index[0]: 4
        index[1]: 9
        index[2]: 16
        index[3]: 25
</script>
```