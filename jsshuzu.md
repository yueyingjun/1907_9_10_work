# javascript
- javascript是基于对象,基于事件驱动，弱类型的解释性语言（弱类型语言可移值性高）
- javascript的定义方式

    关键字定义法
    
    ```
    function  f(){
        方法体
    }
    ```

    直接量

    ```
    var f = function(){
        方法体
    }
    ```
    对象的方式
    ```
    var f = new function(){
        方法体
    }
    ```
    匿名的方式
    ```
    (function(){
        方法体
    })
    ```
- 函数的调用方式
    
    函数名
    ```
    a()
    ```
    自调用
    ```
    (function(){

    }())
    ```
	事件调用
# 数组的方法
- concat 
    数组的拼接,连接,不会改变现有的数组,是将数组拆开一个一个放入新的数组
    ```
    var arr = [1,2,3];
    var arrCopy = arr.concat(4,[5,6]);
    console.log(arrCopy); //[1, 2, 3, 4, 5, 6]
    console.log(arr); // [1, 3, 5, 7](原数组不变)
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
    结果:
        This is an Array
    ```
- copyWithin

    指定位置的元素的复制到其他位置(进行覆盖),改变原数组
    
    arr.copyWithin(target, start, end)
    target 开始覆盖的位置
    start 从该位置开始,默认为0
    end  结束的地方,不包含,默认为数组的最后一个元素
    ```
    将3号位置的元素复制到2号位置
    a = [0,1,2,3,4,5]
    a.copyWithin(2,3,4) 
    结果:
        a = [0, 1, 3, 3, 4, 5]
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

    用固定的值填充数组
    arr.fill(value, start, end)
    value  填充的元素
    start  填充开始的位置，包含
    end    填充结束的位置，不包含，默认为数组的长度
    ```
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.fill("Runoob");
    fruits.fill("Runoob", 2, 4);
    结果:
        Runoob,Runoob,Runoob,Runoob
        Banana,Orange,Runoob,Runoob
    ```
- filter 

    “过滤”功能，数组中的每一项运行给定函数，返回满足过滤条件组成的数组。
    ```
    var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    var arr2 = arr.filter(function(value, index) {
    return index % 3 === 0 || value >= 8;
    }); 
    console.log(arr2); 
    结果:
        1, 4, 7, 8, 9, 10
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
    arr.includes(searchElement, fromIndex)
    fromIndex大于等于数组长度,则返回 false.该数组不会被搜索
    fromIndex 为负值，计算出的索引将作为开始搜索searchElement的位置。如果计算出的索引小于 0，则整个数组都会被搜索。
    ```
    let site = ['runoob', 'google', 'taobao'];
 
    site.includes('runoob'); 
    // true 
    
    site.includes('baidu'); 
    // false
    ```
- indexOf 

    查找某个值在数组中第一次出现的下标，返回值是数据的下标，没有找到则返回-1
    s.indexOf(searchvalue,fromindex)
    fromindex:开始检索的位置
    ```
    var arr = [1,3,5,7,7,5,3,1];
    console.log(arr.indexOf(5)); //2
    console.log(arr.indexOf(5,2)); //2
    console.log(arr.indexOf("5")); //-1
    ```
- join

    将数组的元素组起一个字符串，以separator为分隔符，省略的话则用默认用逗号为分隔符，该方法只接收一个参数：即分隔符
    ```
    var arr = new Array(3)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"

    document.write(arr.join("."))
    结果:
        George.John.Thomas
    ```
- keys 

    返回一个包含索引键的 Array Iterator 对象,
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
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    fruits.entries();
    结果：
        [0, "Banana"]
        [1, "Orange"]
        [2, "Apple"]
        [3, "Mango"]
    ```
- values

    返回一个值的 Array Iterator 对象
    ```
    const array1 = ['a', 'b', 'c'];
    const iterator = array1.values();

    for (const s of iterator) {
        console.log(s); // expected output: "a" "b" "c"
    }
    结果：
        a
        b
        c
    ```

- lastIndexOf

    倒叙查找某个值在数组中第一次出现的位置
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

    删除并返回数组的最后一个元素。
    ```
    var arr = ["George","John","Thomas"];
    var item = arr.pop();
    console.log(item); // Thomas
    console.log(arr); // ["George","John"s]
    ```
- push 

   向数组的末尾追加元素,会修改原数组,返回值：修改后的length值 
    ```
    var arr = ["Lily","lucy","Tom"];
    var count = arr.push("Jack","Sean");
    console.log(count); // 5
    console.log(arr); // ["Lily", "lucy", "Tom", "Jack", "Sean"]
    ```
- reduce 

    方法对累加器和数组中的每个元素（从左到右）应用一个函数，将其简化为单个值。
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
   var arr = new Array(3)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    document.write(arr + "<br />")
    document.write(arr.shift() + "<br />")
    document.write(arr) 
    结果：
        George,John,Thomas
        George
        John,Thomas

    ```
- slice 

    截取字符串
    ```
    var arr = [1,3,5,7,9,11];
    var arrCopy = arr.slice(1);
    var arrCopy2 = arr.slice(1,4);
    console.log(arr); //[1, 3, 5, 7, 9, 11](原数组没变)
    console.log(arrCopy); //[3, 5, 7, 9, 11]
    console.log(arrCopy2); //[3, 5, 7]

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

    删除/添加元素
    arrayObject.splice(index,howmany,item1,.....,itemX)
    index 必需的，位置
    howmany 必须，删除的数量
    item1,.....,itemX 可选，添加新的项目
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
    let str=a.toLocaleString(); 
    结果：
        [object Object],23,abcd,2018/5/28 下午1:52:20
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
    var arr = new Array()
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"

    document.write(arr + "<br />")
    document.write(arr.unshift("William") + "<br />")
    document.write(arr)
    结果：
        George,John,Thomas
        4
        William,George,John,Thomas
    ```
- find

    返回数组中第一个满足回调函数测试的第一个元素的值。否则返回undefined
    ```
    var arr1 = [1, 2, 3, 4, 6, 9];
    let found = arr1.find(e => e > 5); // 6
    ```
- findIndex

    当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。
    ```
    var array1 = [5, 12, 8, 130, 44];
    function isLargeNumber(element) {
    return element > 13;
    }
    console.log(array1.findIndex(isLargeNumber));//3

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

    
- Symbol(Symbol.unscopables)

  