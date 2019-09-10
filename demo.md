# JavaScript 函数
- JS函数的定义方式
    
    1.关键字定义法
```
    function fn(形参){
       方法体
    }

```
  2.直接量

```
    var fn = function(形参){
       方法体
   }

```
  3.对象的方式

```
    var fn = new Function(形参){
       方法体
   }

```
  4.匿名的方式

```
   (function(形参){
       方法体
   })

```
- 函数的调用方式

  1.函数名调用

```
    function fn(形参){
       方法体
    }


   fn()//调用上述定义的方法 

```
  1.函数名调用

```
    function fn(形参){
       方法体
    }


   fn()//调用上述定义的方法 

```
  2.自调用

```
(function(){
    console.log("我是输出的内容")
})()//后比的小括号就是自调用

```
  3.事件调用函数

  - return的作用

    1.终止函数的运行

    2.给函数返回值

# 数组的方法

- concat 

    将参数添加到原数组中
```
    var arr = [1,3,5,7];
    var arrCopy = arr.concat(9,[11,13]);
    console.log(arrCopy); //[1, 3, 5, 7, 9, 11, 13]
    console.log(arr); // [1, 3, 5, 7](原数组未被修改)
```
- constructor 

    返回对创建此对象的数组函数的引用
```
    var test=new Array();
    if (test.constructor==Array){
        document.write("This is an Array");
    }
    if (test.constructor==Boolean){
        document.write("This is a Boolean");
    }
    if (test.constructor==Date){
        document.write("This is a Date");
    }
    if (test.constructor==String){
        document.write("This is a String");
    }
```
- copyWithin

    方法浅复制数组的一部分到同一数组中的另一个位置，并返回它，而不修改其大小。会改变原数组。
```
    arr.copyWithin(target[, start[, end]])
    target //从哪个地方修改，从0开始计算
    start //从哪里开始复制，从0开始计算
    end  //从哪里结束复制，从0开始计算，不包括这个下标值

    a = [0,1,2,3,4,5]
    a.copyWithin(3,0,2)   // [0, 1, 2, 0, 1, 5]  从第三个位置修改0~2(0,1)。
    a //[0, 1, 2, 0, 1, 5]  改变原数组
```
- every 

    判断数组中每一项都是否满足条件，只有所有项都满足条件，才会返回true。
```
    var arr = [1, 2, 3, 4, 5];
    var arr2 = arr.every(function(x) {
    return x < 10;
    }); 
    console.log(arr2); //true
    var arr3 = arr.every(function(x) {
    return x < 3;
    }); 
    console.log(arr3); // false
```
- fill

    用一个固定值填充一个数组中从起始索引到终止索引内的全部元素。
```
    arr.fill(value[, start[, end]])
    [1, 2, 3].fill(4);               // [4, 4, 4] 替换值为4
    [1, 2, 3].fill(4, 1);            // [1, 4, 4] 替换值为4，位置从1~3(不包括)
    [1, 2, 3].fill(4, 1, 2);         // [1, 4, 3] 替换值为4，位置从1~2(不包括)
    [1, 2, 3].fill(4, 1, 1);         // [1, 2, 3] 替换值为4，位置从1~1(不包括)
    [1, 2, 3].fill(4, 3, 3);         // [1, 2, 3] 替换值为4，位置从3~3(不包括)
    [1, 2, 3].fill(4, -3, -2);       // [4, 2, 3] 位置从(3+-3)~(3+-2)=>0~1(不包括)
    [1, 2, 3].fill(4, NaN, NaN);     // [1, 2, 3] 替换值4,
    [1, 2, 3].fill(4, 3, 5);         // [1, 2, 3] 替换值为4 从4~5(不包括)
```
- filter 

    “过滤”功能，数组中的每一项运行给定函数，返回满足过滤条件组成的数组。
```
    var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    var arr2 = arr.filter(function(x, index) {
    return index % 3 === 0 || x >= 8;
    }); 
    console.log(arr2); //[1, 4, 7, 8, 9, 10]
```
- forEach 

    对数组进行遍历循环，对数组中的每一项运行给定函数。这个方法没有返回值
```
    var arr = [1, 2, 3, 4, 5];
    arr.forEach(function(x, index, a){
    console.log(x + '|' + index + '|' + (a === arr));
    });
    // 输出为：
    // 1|0|true
    // 2|1|true
    // 3|2|true
    // 4|3|true
    // 5|4|true
```
- includes

    返回一个布尔值，表示某个数组是否包含给定的值
```
    let a=['OB','Koro1',1,NaN];
    // let b=a.includes(NaN); // true 识别NaN
    // let b=a.includes('Koro1',100); // false 超过数组长度 不搜索
    // let b=a.includes('Koro1',-3); // true 从倒数第三个元素开始搜索 
    // let b=a.includes('Koro1',-100); // true 负值绝对值超过数组长度，搜索整个数组
```
- indexOf 

    接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的开头（位置 0）开始向后查找。 
```
    var arr = [1,3,5,7,7,5,3,1];
    console.log(arr.indexOf(5)); //2
    console.log(arr.indexOf(5,2)); //2
    console.log(arr.indexOf("5")); //-1
```
- join

    将数组的元素组起一个字符串，以separator为分隔符，省略的话则用默认用逗号为分隔符，该方法只接收一个参数：即分隔符
```
    var arr = [1,2,3];
    console.log(arr.join()); // 1,2,3
    console.log(arr.join("-")); // 1-2-3
    console.log(arr); // [1, 2, 3]（原数组不变）

```
- keys 

    返回一个新的 Array Iterator 对象
```
    array.keys()
    for (let index of ['a', 'b'].keys()) {
 console.log(index);
}
// 0
// 1
```
- entries

    返回一个新的Array Iterator对象，该对象包含数组中每个索引的键/值对。
```
array.entries()
for (let [index, elem] of ['a', 'b'].entries()) {
 console.log(index, elem);
}
// 0 "a"
// 1 "b"
```
- values

    返回一个新的 Array Iterator 对象
```
    array.values()
    for (let elem of ['a', 'b'].values()) {
    console.log(elem);
    }
    // 'a'
    // 'b'
```

- lastIndexOf

    接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的末尾开始向前查找。
```
    var arr = [1,3,5,7,7,5,3,1];
    console.log(arr.lastIndexOf(5)); //5
    console.log(arr.lastIndexOf(5,4)); //2
```
- length

    输出数组的长度
```
    var arr=[11,1,1,1,1,1,"a"]
    console.log(arr);//7
```
- map 

    指“映射”，对数组中的每一项运行给定函数，返回每次函数调用的结果组成的数组。
``` 
    var arr = [1, 2, 3, 4, 5];
    var arr2 = arr.map(function(item){
    return item*item;
    });
    console.log(arr2); //[1, 4, 9, 16, 25]
```
- pop 

    数组末尾移除最后一项，减少数组的 length 值，然后返回移除的项。
```
    var arr = ["Lily","lucy","Tom"];
    var item = arr.pop();
    console.log(item); // Sean
    console.log(arr); // ["Lily", "lucy", "Tom", "Jack"]
```
- push 

    可以接收任意数量的参数，把它们逐个添加到数组末尾，并返回修改后数组的长度。 
```
    var arr = ["Lily","lucy","Tom"];
    var count = arr.push("Jack","Sean");
    console.log(count); // 5
    console.log(arr); // ["Lily", "lucy", "Tom", "Jack", "Sean"]
```
- reduce 

    从数组的第一项开始，逐个遍历到最后
```
    var values = [1,2,3,4,5];
    var sum = values.reduce(function(prev, cur, index, array){
    return prev + cur;
    },10);
    console.log(sum); //25
```
- reduceRight 

    从数组的最后一项开始，向前遍历到第一项。
```
    var values = [1,2,3,4,5];
    var sum = values.reduceRight(function(prev, cur, index, array){
    return prev + cur;
    },10);
    console.log(sum); //25
```
- reverse

    颠倒数组中元素的顺序
```
    let a = [1,2,3];
    a.reverse(); 
    console.log(a); // [3,2,1]
```
- shift 

    删除原数组第一项，并返回删除元素的值；如果数组为空则返回undefined 。
```
    var arr = ["Lily","lucy","Tom"];
    var item = arr.shift();
    console.log(item); // Jack
    console.log(arr); // ["Sean", "Lily", "lucy", "Tom"]

```
- slice 

    返回从原数组中指定开始下标到结束下标之间的项组成的新数组。slice()方法可以接受一或两个参数，即要返回项的起始和结束位置。在只有一个参数的情况下， slice()方法返回从该参数指定位置开始到当前数组末尾的所有项。如果有两个参数，该方法返回起始和结束位置之间的项——但不包括结束位置的项。
```
    var arr = [1,3,5,7,9,11];
    var arrCopy = arr.slice(1);
    var arrCopy2 = arr.slice(1,4);
    var arrCopy3 = arr.slice(1,-2);
    var arrCopy4 = arr.slice(-4,-1);
    console.log(arr); //[1, 3, 5, 7, 9, 11](原数组没变)
    console.log(arrCopy); //[3, 5, 7, 9, 11]
    console.log(arrCopy2); //[3, 5, 7]
    console.log(arrCopy3); //[3, 5, 7]
    console.log(arrCopy4); //[5, 7, 9]

```
- some 

    判断数组中是否存在满足条件的项，只要有一项满足条件，就会返回true。
```
    var arr = [1, 2, 3, 4, 5];
    var arr2 = arr.some(function(x) {
    return x < 3;
    }); 
    console.log(arr2); //true
    var arr3 = arr.some(function(x) {
    return x < 1;
    }); 
    console.log(arr3); // false
```
- sort 

    按升序排列数组项——即最小的值位于最前面，最大的值排在最后面。
    在排序时，sort()方法会调用每个数组项的 toString()转型方法，然后比较得到的字符串，以确定如何排序。即使数组中的每一项都是数值， sort()方法比较的也是字符串，因此会出现以下的这种情况：
```
    var arr1 = ["a", "d", "c", "b"];
    console.log(arr1.sort()); // ["a", "b", "c", "d"]
    arr2 = [13, 24, 51, 3];
    console.log(arr2.sort()); // [13, 24, 3, 51]
    console.log(arr2); // [13, 24, 3, 51](元数组被改变)

    升序：
    function compare(value1, value2) {
    if (value1 < value2) {
    return -1;
    } else if (value1 > value2) {
    return 1;
    } else {
    return 0;
    }
    }
    arr2 = [13, 24, 51, 3];
    console.log(arr2.sort(compare)); // [3, 13, 24, 51]
```
- splice 

    很强大的数组方法，它有很多种用法，可以实现删除、插入和替换。
```
    var arr = [1,3,5,7,9,11];
    var arrRemoved = arr.splice(0,2);
    console.log(arr); //[5, 7, 9, 11]
    console.log(arrRemoved); //[1, 3]
    var arrRemoved2 = arr.splice(2,0,4,6);
    console.log(arr); // [5, 7, 4, 6, 9, 11]
    console.log(arrRemoved2); // []
    var arrRemoved3 = arr.splice(1,1,2,4);
    console.log(arr); // [5, 2, 4, 4, 6, 9, 11]
    console.log(arrRemoved3); //[7]
```
- toLocaleString

    返回一个表示数组元素的字符串。
```
    let a=[{name:'OBKoro1'},23,'abcd',new Date()];
    let str=a.toLocaleString(); // [object Object],23,abcd,2018/5/28 下午1:52:20
```
- toString

    可把数组转换为由逗号链接起来的字符串。
```
    let b= [ 'toString','演示'].toString(); // toString,演示
    let a= ['调用toString','连接在我后面']+'啦啦啦'; // 调用toString,连接在我后面啦啦啦
```
- unshift 

    将参数添加到原数组开头，并返回数组的长度 。
```
    var arr = ["Lily","lucy","Tom"];
    var count = arr.unshift("Jack","Sean");
    console.log(count); // 5
    console.log(arr); //["Jack", "Sean", "Lily", "lucy", "Tom"]
```
- find

    为数组中的每个元素都调用一次函数执行：
```
    var ages = [3, 10, 18, 20];
    function checkAdult(age) {
        return age >= 18;
    }
    function myFunction() {
        document.getElementById("demo").innerHTML = ages.find(checkAdult);
    }//18
```
- findIndex

    当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
```
    var ages = [3, 10, 18, 20];
    function checkAdult(age) {
        return age >= 18;
    }
    function myFunction() {
        document.getElementById("demo").innerHTML = ages.findIndex(checkAdult);
    }//2
```
- flat

    将多维数组转化为一维数组
```
    let ary = [1, [2, [3, [4, 5]]], 6];
    let str = JSON.stringify(ary);
    第0种处理:直接的调用
    arr_flat = arr.flat(Infinity);
    第一种处理
    ary = str.replace(/(\[\]))/g, '').split(',');
    第二种处理
    str = str.replace(/(\[\]))/g, '');
    str = '[' + str + ']';
    ary = JSON.parse(str);
    第三种处理：递归处理
    let result = [];
    let fn = function(ary) {
    for(let i = 0; i < ary.length; i++) }{
    let item = ary[i];
    if (Array.isArray(ary[i])){
    fn(item);
    } else {
    result.push(item);
    }
    }
    }
    第四种处理：用 reduce 实现数组的 flat 方法
    function flatten(ary) {
    return ary.reduce((pre, cur) => {
    return pre.concat(Array.isArray(cur) ? flatten(cur) : cur);
    })
    }
    let ary = [1, 2, [3, 4], [5, [6, 7]]]
    console.log(ary.MyFlat(Infinity))
    第五种处理：扩展运算符
    while (ary.some(Array.isArray)) {
    ary = [].concat(...ary);
    }
```
- flatMap

    是javascript中的内置函数，用于将输入数组元素展平为新数组
```
var A = [ 1, 2, 3, 4, 5 ];  
    b = A.map(x => [x * 3]); 
    document.write(b);  
    c = arr1.flatMap(x => [x * 3]); 
    document.write(c);  
    d = arr1.flatMap(x => [[ x * 3 ]]); 
    document.write(d); 
    //[[3]，[6]，[9]，[12]，[15]] 
[3,6,9,12,15] 
[[3]，[6]，[9]，[12]，[ 15]
```
- Symbol(Symbol.iterator)

    当需要对一个对象进行迭代时（比如开始用于一个for..of循环中），它的@@iterator方法都会在不传参情况下被调用，返回的迭代器用于获取要迭代的值。
```
    var myIterable = {}
    myIterable[Symbol.iterator] = function* () {
        yield 1;
        yield 2;
        yield 3;
    };
    [...myIterable] // [1, 2, 3]
```
- Symbol(Symbol.unscopables)

    指用于指定对象值，其对象自身和继承的从关联对象的 with 环境绑定中排除的属性名称。
```
    var obj = { 
    foo: 1, 
    bar: 2 
    };
    obj[Symbol.unscopables] = { 
    foo: false, 
    bar: true 
    };
    with (obj) {
    console.log(foo); // 1
    console.log(bar); // ReferenceError: bar is not defined
    }
```