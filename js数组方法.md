

# js数组方法

#### 	创建数组的方法

###### 			构造函数	

```javascript
			var array= new Array();
			var array1= new Array(20);
			var array2= new Array("1","2");
			
```

###### 			字面量表示法

```javascript
			var arr6= ["a","b","c"];
```

###### 			判断是否为数组的方法  

###### 				(1)  instanceof Array

```
				console.log(array instanceof Array)
```

###### 				(6) Array.isArray()  

```
				console.log(Array.isArray()
```

#### 	 数组方法

###### 			join()  将数组整理成字符串（跟字符串方法split()相对应）

​			-只接受一个参数，及分隔符

```
			var arr=[1,2,3]
			console.log(arr.join()) //1,2,3
			console.log(arr.join("-")) // 1-2-3
			console.log(arr);//[1,2,3]元素组不变
```

###### 			push()和pop  

###### 			push方法是对数组新增作用，新值加到数组最后，返回值是新的数组长度，参数可以是任意类型

```
			var arr=["a","b","c"]
			var count = arr.push("d")
			console.log(count);//4
			console.log(arr);//["a","b","c","d"];
```

###### 			pop()方法是对数组进行删除，删除最后一位，减少数组的长度，然后返回移除的项，不接受任何参数			

```
			var item=arr.pop();
			console.log(item);// d
			console.log(arr);//["a","b","c"]
```

###### 			shift()和unshift()

###### 			shift:删除原数组的第一项，并返回删除元素的值；如果数组为空则返回undefined

###### 			unshift：将参数添加到原数组开头。并返回数组的长度			

```javascript
			var arr=["a","b","c"];
			var count=arr.unshift("A");
			console.log(count);//4
			console.log(arr);//["A","a","b","c"]
			var item =arr.shift();
			console.log(item);"A"
			console.log(arr);["a","b","c"]
```

###### 			sort()

###### 			将数组内部数组进行排序（可接受函数）

```
			var arr=["a","b","c"];
			console.log(arr.sort())//["a","b","c"]
```

###### 			sort()方法会调用每个数组项的tostring()转型方法

###### 			sort()方法可以接受一个比较函数作为参数，以便我们指定哪个值位于哪个值的前面。比较函数接收两个参数，如果第一个参数应该位		于第二个之前则返回一个负数，如果两个参数相等则返回 0，如果第一个参数应该位于第二个之后则返回一个正数。以下就是一个简单的比		较函数。

```
			function compare(value1,value2){
                if(value1<value2){
                    return -1;
                }else if(value1 >values2){
                    return 1;
                }else{
                    return 0;
                }
			}
			arr =[12,23,51,3]
			console.log(arr.sort(compare)//[3,12,23,51]
```

###### 			reverse()

###### 			将数组内容完全反转（不接受参数）

```
            var arr = [13, 24, 51, 3];
            console.log(arr.reverse()); //[3, 51, 24, 13]
            console.log(arr); //[3, 51, 24, 13]
```

###### 			concat（）将参数添加到原数组中，这个方法会先创建当前数组一个副本，然后将接收到的参数添加到这和副本的末尾，最后返回新构		建的数组。在没有给concat（）方法传递参数的情况下，它只是复制当前数组并返回副本

```
		var arr=[1,3,5,7]
        var arrCopy= arr.concat(9,[11,13])
        console.log(arrCopy)//[1,3,5,7,9,11,13]
        console.log(arr);//[1,3,5,7]原数组未修改
```

###### 			如果传入的是一个二维数组，那么也会把这一数组项当作一项添加到Array中

```
			var arr2 = arr1.concat([9,[22,33]]);
			console.log(arr)//[1,3,5,7,arr2]
			console.log(arr[5]);//[22,33]
```

###### 			slice()

###### 			返回从原数组中指定开始下标到结束下标之间的项组成的新数组

```
		var arr = [1,3,5,7,9,11];
		console.log(arr); //[1, 3, 5, 7, 9, 11]
		var arrCopy = arr.slice(1);//如果只写第一个参数的话，这个表示从数组第二位到数组最后一位
		console.log(arrCopy); //[3, 5, 7, 9, 11]
		var arrCopy2 = arr.slice(1,4);//从数组第二位开始（包括第二位）到第四位（不包括第四位）截取数组
		console.log(arrCopy2); //[3, 5, 7]
		var arrCopy3 = arr.slice(1,-2);//复数表示从数组最后往前算，-1表示数组最后一位，这里的-2表示数组倒数第二位（负值的话，跟数组长度相加，也能是相同效果，等同于arr.slice(1,4)）
		console.log(arrCopy3); //[3, 5, 7]
		var arrCopy4= arr.slice(-4,-1)
		console.log(arrCopy4); //[5,7,9]
```

###### 			splice()

###### 			很强大的数组方法，它有很多中用法， 可是实现删除，插入和替换（原数组会变化）

###### 			　array.splice(index,howmany,item1,.....,itemX) 

　　　　　　　　index表示数组要更正的起始位置，（必填）

　　　　　　　howmany：表示从起始位置之后需要替换/删除的的数量，如果是0的话，不会进行删除操作；

　　　　　　　item1,.....,itemX（选填，如果不填的话，只有前面的话，表示从index开始，进行删除，数量为howmany）如果写的话，表示在前删除			操作做完之后把这些方法删除位置。进行插入替换，

```
            var arr = [1,3,5,7,9,11];
            var arrRemoved = arr.splice(0,2);
            console.log(arr); //[5, 7, 9, 11] 改变了原数组
            console.log(arrRemoved); //[1, 3] 返回值是截取的数值组成的数组
            
            var arrRemoved2 = arr.splice(2,0,4,6); ？？？？
            console.log(arr); // [5, 7, 4, 6, 9, 11] 如果是0的话，会将后面的数值插入到index的前面
            console.log(arrRemoved2); // []
            
            var arrRemoved3 = arr.splice(1,1,2,4);？？？
            console.log(arr); // [5, 2, 4, 4, 6, 9, 11]
            console.log(arrRemoved3); //[7]
```

###### 			indexOf()和latIndexOf()

###### 			indexOf()：接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的开头（位置 0）开始向后查找。 
　　　　　      lastIndexOf：接收两个参数：要查找的项和（可选的）表示查找起点位置的索引。其中， 从数组的末尾开始向前查找。		

###### 　　　　　 这两个方法都返回要查找的项在数组中的位置，或者在没找到的情况下返回-1。（只会找到第一个匹配项）在比较第一个参数与数组中的	每一项时，会使用全等操作符（类型也会进行比较的）。

```
			var arr = [1,3,5,7,7,5,3,1];
            console.log(arr.indexOf(5)); //2 第一个5的位置
            console.log(arr.lastIndexOf(5)); //5  最后一个5的位置
            console.log(arr.indexOf(5,2)); //2  查询5  从第2个从开始查找  下标为2  
            console.log(arr.indexOf(5,3)); //5  
            console.log(arr.indexOf(5,10)); //-1
            console.log(arr.lastIndexOf(5,4)); //2
            console.log(arr.indexOf("5")); //-1
```

###### 			map（）

###### 			指“映射”，对数组中的每一项运行给定函数，返回每次函数调用的结果组成的数组。

###### 			有return的话，返回值会组成一个新数组，如果没有返回值的话，也会有一个同长度的新数组，不过每一项都是undifined；

　　　　　 跟forEach()方法类似，不过map有返回值。

```
			var arr = [1, 2, 3, 4, 5];
			var arr2 = arr.map(function(item，index，a){//跟foreach一样的参数
			return item*item;
				});
			console.log(arr2); //[1, 4, 9, 16, 25]
```

###### 			filter()

###### 			“过滤”功能，数组中的每一项运行给定函数，返回满足过滤条件组成的数组。(不改变原数组)

```
			var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
			var arr2 = arr.filter(function(x, index) {
			return index % 3 === 0 || x >= 8;
				}); 
			console.log(arr2); //[1, 4, 7, 8, 9, 10]
```

###### 			every()

###### 			判断数组中每一项都是否满足条件，只有所有项都满足条件，才会返回true。（不改变原数组）

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

###### 			some()

###### 			判断数组中是否存在满足条件的项，只要有一项满足条件，就会返回true。（不改变原数组）

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

###### 			reduce()和reduceRight（）

###### 			作用：这两个方法都会实现迭代数组的所有项，然后构建一个最终返回的值。reduce()方法从数组的第一项开始，逐个遍历到最后。而 reduceRight()则从数组的最后一项开始，向前遍历到第一项。

###### 　　　　　　  这两个方法都接收两个参数：一个在每一项上调用的函数和（可选的）作为归并基础的初始值。

###### 　　　　　　  传给 reduce()和 reduceRight()的函数接收 4 个参数：前一个值、当前值、项的索引和数组对象。这个函数返回的任何值都会作为第一个参数自动传给下一项。第一次迭代发生在数组的第二项上，因此第一个参数是数组的第一项，第二个参数就是数组的第二项。

　　　　　　  下面代码用reduce()实现数组求和，数组一开始加了一个初始值10。

```
            var values = [1,2,3,4,5];
            var sum = values.reduceRight(function(prev, cur, index, array){
            return prev + cur;
            },10);//这个10会当作循环第一次回调函数里面的prev值
            console.log(sum); //25　
```

```
			
```

​				