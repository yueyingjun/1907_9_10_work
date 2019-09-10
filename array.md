# 数组的方法
* push() <br>
  在数组结尾处添加一个新元素
```
var arr = [1,2,3];
fruits.push(4);
```
* concat()<br>
连接两个或多个数组，并返回结果
```
var arr1 = [1,2];
var arr2 = [3,4];
var arr3=[];
var arr = arr3.concat(arr1,arr2);
console.log(arr);
```
* copyWithin()<br>
从数组的一个指定位置拷贝元素到另一个指定的位置
  * 语法：array.copyWithin(target, start, end)
  * target复制到指定位置的索引
  * start 复制的起始位置
  * end 停止位置的索引
```
var arr= ["a","b","c","d"];
arr.copyWithin(2,0,3);

输出 arr=["a","b","a","b"]
```
* entries() <br>
返回一个数组的迭代对象，该对象包含数组的键值对 (key/value)。
 迭代对象中数组的索引值作为 key， 数组元素作为 value。
```
var arr = [1,2,3];
arr.entries();

输出：
    0: 1
    1: 2
    2: 3
    length: 3
```
* every()<br>
用于检测数组所有元素是否都符合指定条件（通过函数提供）
  * 如果有一个不满足，返回false
  * 全部满足，返回true
  * 不能对空数组进行检查
```
var arr=[1,2,3,4];
function f(num){
  return num>2;
}
var flag=arr.every(f);

输出 false
```
* fill()<br>
使用一个固定的值来填充数组。
    * array.fill(value, start, end)；
```
var arr=[1,2,3];
arr.fill(4,1,3);

输出：arr=[1,4,4];
```
* filter()<br>
创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
    * 语法array.filter(function(currentValue,index,arr), thisValue)
```
var arr=[1,2,3,4];
function f(num){
  return num>2;
}
var arr1=arr.filter(f);

输出[3,4]
```
* find() <br>
返回通过测试（函数内判断）的数组的第一个元素的值。
```
var arr=[1,2,3,4];
function f(num){
  return num>2;
}
var arr1=arr.find(f);

输出 3
```
* findIndex()<br>
返回传入一个测试条件（函数）符合条件的数组第一个元素位置。
```
var arr=[1,2,3,4];
function f(num){
  return num>2;
}
var arr1=arr.findIndex(f);

输出 2
```
* forEach()<br>
 方法用于调用数组的每个元素，并将元素传递给回调函数。
```

```
* from()<br>
用于通过拥有 length 属性的对象或可迭代的对象来返回一个数组。
```
var arr = Array.from("a");
```
* includes() <br>
用来判断一个数组是否包含一个指定的值，如果是返回 true，否则false。 
```
var arr = ["a", "b", "c"];
arr.includes("b"); 

输出 true
```
* indexOf() <br>
可返回数组中某个指定的元素位置。
```
var arr = ["a", "b", "c"];
var arr1 = arr.indexOf("a");

输出  0
```
* isArray()<br>
用于判断一个对象是否为数组。
```
 var arr = ["a", "b", "c"];
 var flag=Array.isArray(arr);
 console.log(flag);
 
 输出  true
```
* join()<br>
把数组中的所有元素放进一个字符串。
```
var arr = ["a", "b", "c"];
var arr1 = arr.join();

输出  abc
```
* keys()<br>
返回数组的可迭代对象，包含原始数组的键(key)。
```
var arr = [1,2,3];
arr.keys();

```
* lastIndexOf()<br>
搜索数组中的元素，并返回它最后出现的位置。
```
var arr = [1,2,3,4,2,5,6];
var a= arr.lastIndexOf(2);

输出 4
```
* map()<br>
	通过指定函数处理数组的每个元素，并返回处理后的数组。
```
var arr1 = [4,9,16];
var arr2 = arr1.map(Math.sqrt);

输出 2,3,4
```
* pop()<br>
删除数组的最后一个元素并返回删除的元素。
```
var arr= [1,2,3,4];
arr.pop()

输出 arr=[1,2,3]
```
* reduce()<br>
将数组元素计算为一个值（从左到右）。
```

```
* reduceRight()<br>
将数组元素计算为一个值（从右到左）。
```

```
* reverse()<br>
反转数组的元素顺序。
```
var arr = [1,2,3];
arr.reverse;

输出：3,2,1
```
* shift()<br>
删除并返回数组的第一个元素。
```
var arr = [1,2,3];
arr.shift();

输出 2,3
```
* slice()<br>
选取数组的的一部分，并返回一个新数组。
  *array.slice(start, end)
```
var arr=[1,2,3,4];
var arr1 = arr.slice(1,3);

输出 arr1=[2,3]

```
* some()<br>
检测数组元素中是否有元素符合指定条件。
```
 var arr = [1,2,3,4];
    function f(num) {
        return num>3;
    }
    var flag = arr.some(f);
    console.log(flag);
    
    输出  true
```
* sort()<br>
对数组的元素进行排序。
   * 和回调函数一起使用比较合适
```
  var arr=[22,35,4,1,72,9];
        arr.sort();
        console.log(arr);
        arr.sort(function (a,b) {
            return a-b;// b-a降序
        });
        console.log(arr);
```
* splice()<br>
从数组中添加或删除元素。
  * 语法：array.splice(index,howmany,item1,.....,itemX)
  * splice(2,1) 删除1个
  * howmany 删除多少个
  * item 添加的元素
```
var arr=[1,2,3,4];
arr.splice(2,0,5);

输出 arr=[1,2,5,3,4]
```
* toString()<br>
把数组转换为字符串，并返回结果。
```
var arr = ["a","b","c"];
arr.toString();

输出 a,b,c
```
*  unshift()<br>
向数组的开头添加一个或更多元素，并返回新的长度。
```
var arr=[1,2,3];
arr.unshift(5,4,6);

输出 [5,4,6,1,2,3] 
```
* valueOf()<br>
```
var arr= [1,2,3];
var arr1 = arr.valueOf();

输出 1,2,3
```
* flat()<br>
使数组扁平化
```
var arr=[1,[1,2],[2,3]];
var arr1 = arr.flat();

输出 [1,1,2,2,3]
```
* flatMap()<br>
与map相似
```

```
* toLocaleString()<br>
根据本地时间把 Date 对象转换为字符串，并返回结果。
```
var date = new Date();
document.write(date.toLocaleString())

输出 2019/9/10 下午10:41:08
```
* values()<br>
获取数组的元素值
```
var arr = [1,2,4];
    var iterator = arr.values();
    for (let elem of iterator) {
        console.log(elem);
    }
    
 输出
 1
 2
 4
```
