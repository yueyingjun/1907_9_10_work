# 数组的方法

### concat 

​	将参数添加到原数组中。

```
    var arr = [1,3,5,7];
    var arrCopy = arr.concat(9,[11,13]);
    console.log(arrCopy); //[1, 3, 5, 7, 9, 11, 13]
    console.log(arr); // [1, 3, 5, 7](原数组未被修改)
```

### constructor 

​	返回对创建此对象的数组函数的引用。

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

### copyWithin

​	方法浅复制数组的一部分到同一数组中的另一个位置，并返回它，而不修改其大小。会改变原数组。

```
	arr.copyWithin(target[, start[, end]])
    target //从哪个地方修改，从0开始计算
    start //从哪里开始复制，从0开始计算
    end  //从哪里结束复制，从0开始计算，不包括这个下标值

    var a = [0,1,2,3,4,5,6]
    a.copyWithin(3,0,2)   // [0, 1, 2, 0, 1, 5, 6]  从第三个位置修改0~2(0,1)。
    console.log(a); //[0, 1, 2, 0, 1, 5, 6]  改变原数组
```

### find

​	为数组中的每个元素都调用一次函数执行。

```
    var ages = [3, 10, 18, 20];
    function checkAdult(age) {
        return age >= 18;
    }
    function myFunction() {
        document.getElementById("demo").innerHTML = ages.find(checkAdult);
    } //18
```

### fill

​	用一个固定值填充一个数组中从起始索引到终止索引内的全部元素。

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

### filter

​	“过滤”功能，数组中的每一项运行给定函数，返回满足过滤条件组成的数组。

```
    var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    var arr2 = arr.filter(function(x, index) {
    	return index % 3 === 0 || x >= 8;
    }); 
    console.log(arr2); //[1, 4, 7, 8, 9, 10]
```

### forEach

​	对数组进行遍历循环，对数组中的每一项运行给定函数。这个方法没有返回值。

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

### indexOf

​	接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的开头（位置 0）开始向后查找。 

```
    var arr = [1,3,5,7,7,5,3,1];
    console.log(arr.indexOf(5)); //2
    console.log(arr.indexOf(5,2)); //2
    console.log(arr.indexOf("5")); //-1
```

### join

​	将数组的元素组起一个字符串，以separator为分隔符，省略的话则用默认用逗号为分隔符，该方法只接收一个参数：即分隔符。

```
    var arr = [1,2,3];
    console.log(arr.join()); // 1,2,3
    console.log(arr.join("/")); // 1/2/3
    console.log(arr); // [1, 2, 3]（原数组不会发生改变）
```

### entries

​	返回一个新的Array Iterator对象，该对象包含数组中每个索引的键/值对。

```
	array.entries()
	for (let [index, elem] of ['a', 'b'].entries()) {
	 	console.log(index, elem);
	}
	// 0 "a"
	// 1 "b"
```

### values

​	返回一个新的 Array Iterator 对象。

```
    array.values()
    for (let elem of ['a', 'b'].values()) {
    	console.log(elem);
    }
    // 'a'
    // 'b'
```

### length

​	输出数组的长度。

        var arr=[11,1,1,1,1,1,"a"]
        console.log(arr);//7
### map

​	指“映射”，对数组中的每一项运行给定函数，返回每次函数调用的结果组成的数组。

        var arr = [1, 2, 3, 4, 5];
        var arr2 = arr.map(function(item){
        	return item*item;
        });
        console.log(arr2); //[1, 4, 9, 16, 25]
### lastIndexOf

​	接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的末尾开始向前查找。

```
    var arr = [1,3,5,7,7,5,3,1];
    console.log(arr.lastIndexOf(5)); //5
    console.log(arr.lastIndexOf(5,4)); //2
```

### push

​	可以接收任意数量的参数，把它们逐个添加到数组末尾，并返回修改后数组的长度。 

```
    var arr = ["Lily","lucy","Tom"];
    var count = arr.push("Jack","Sean");
    console.log(count); // 5
    console.log(arr); // ["Lily", "lucy", "Tom", "Jack", "Sean"]
```

### reduce

​	从数组的第一项开始，逐个遍历到最后。

```
    var values = [1,2,3,4,5];
    var sum = values.reduce(function(prev, cur, index, array){
    	return prev + cur;
    },10);
    console.log(sum); //25
```

### reduceRight

​	从数组的最后一项开始，向前遍历到第一项。

```
    var values = [1,2,3,4,5];
    var sum = values.reduceRight(function(prev, cur, index, array){
    	return prev + cur;
    },10);
    console.log(sum); //25
```

### reverse

​	颠倒数组中元素的顺序。

```
    var a = [1,2,3];
    a.reverse(); 
    console.log(a); // [3,2,1]
```

### sort

​	按升序排列数组项——即最小的值位于最前面，最大的值排在最后面。在排序时，sort()方法会调用每个数组项的 toString()转型方法，然后比较得到的字符串，以确定如何排序。即使数组中的每一项都是数值， sort()方法比较的也是字符串，因此会出现以下的这种情况：

```
    var arr1 = ["a", "d", "c", "b"];
    console.log(arr1.sort()); // ["a", "b", "c", "d"]
    arr2 = [13, 24, 51, 3];
    console.log(arr2.sort()); // [13, 24, 3, 51]
    console.log(arr2); // [13, 24, 3, 51](原数组会改变)
    
    >=0倒序；<0正序
    arr2.sort(function (a,b){
		return a-b
	})
	var a= ['调用toString','连接在我后面']+'啦啦啦'; // [3, 13, 24, 51]
```

### toString

​	可把数组转换为由逗号链接起来的字符串。

```
    var b= [ 'toString','演示'].toString(); // toString,演示
    var a= ['调用toString','连接在我后面']+'啦啦啦';
    console.log(a); // 调用toString,连接在我后面啦啦啦
```