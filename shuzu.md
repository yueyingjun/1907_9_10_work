#数组
##1、length：计算出数组的长度。下列num就是a数组的长度。
```
    var a=[1,2,3]
    var num=a.length
```
##2、concat：方法用于连接两个或多个数组。返回值是一个新的数组。a就是将c连接到b后的新数组
```
    var c=[1,2,3]
    var b=[4,5,6]
    var a=c.concat(b)
    console.log(a)
```
##3、constructor:返回对创建此对象的数组函数的引用。text就是a的类型

```
    var a=new Array();
    var text=a.constructor
```
##4、copyWithin() 方法用于从数组的指定位置拷贝元素到数组的另一个指定位置中。target：必需。复制到指定目标索引位置。start	可选。元素复制的起始位置。end	可选。停止复制的索引位置 (默认为 array.length)。如果为负值，表示倒数。
```
    var a=[1,2,3,4,5,6]
    a.copyWithin(target, start, end)

```
##5、entries() 方法返回一个数组的迭代对象，该对象包含数组的键值对 (key/value)。
```
    var a=[1,2,3,4,5,6]
    console.log(Object.entries(a));
```
##6、every() 方法用于检测数组所有元素是否都符合指定条件（通过函数提供）。every() 方法使用指定函数检测数组中的所有元素：
```
     var a=[1,2,3,4,5,6]
    a.every(function(){})
```
##7、fill() 方法用于将一个固定值替换数组的元素。三个参数，第一个为替换值，第二、三个为替换位置（包含前不包含后）
```
    var a = ["Banana", "Orange", "Apple", "Mango"];
    a.fill("Runoob", 1, 3);
```
##8、filter() 方法创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
``` 
    var a=[1,2,3,4,5,6]
    a.filter(checkAdult(){});

```
##9、find() 方法返回通过测试（函数内判断）的数组的第一个元素的值。 当数组中的元素在测试条件时返回 true 时, find() 返回符合条件的元素，之后的值不会再调用执行函数。如果没有符合条件的元素返回 undefined。
```
    var ages = [3, 10, 18, 20];
    ages.find(checkAdult(){})
 
```
##10、findIndex() 方法返回传入一个测试条件（函数）符合条件的数组第一个元素位置。findIndex() 方法为数组中的每个元素都调用一次函数执行：当数组中的元素在测试条件时返回 true 时, findIndex() 返回符合条件的元素的索引位置，之后的值不会再调用执行函数。如果没有符合条件的元素返回 -1。
```
    var ages = [3, 10, 18, 20];
    ages.findIndex(checkAdult(){});

```
##11、flat() 方法会按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的子数组中的元素合并为一个新数组返回。
```
    var newArray = arr.flat([depth])
```
##12、flatMap() 方法首先使用映射函数映射每个元素，然后将结果压缩成一个新数组。它与 map 和 深度值1的 flat 几乎相同，但 flatMap 通常在合并成一种方法的效率稍微高一些。
```
    

```
##13、forEach() 方法用于调用数组的每个元素，并将元素传递给回调函数。a:必需。 一个数组对象。callbackfn:必需。 一个接受最多三个参数的函数。 对于数组中的每个元素，forEach 都会调用 callbackfn 函数一次。thisArg:可选。 可在 callbackfn 函数中为其引用 this 关键字的对象。 如果省略 thisArg，则 undefined 将用作 this 值。

```
    a.forEach(callbackfn[, thisArg])
```
##14、includes() 方法用来判断一个数组是否包含一个指定的值，如果是返回 true，否则false。
```
    var a=[1,2,3]
    a.includes()

```
##15、indexOf() 方法可返回某个指定的字符串值在字符串中首次出现的位置。indexOf() 方法对大小写敏感！
 ```
    arr.join()
    str.indexOf("Hello")
```   
    
##16、join() 方法用于把数组中的所有元素放入一个字符串。
```
   var arr = new Array(3)
   arr[0] = "George"
   arr[1] = "John"
   arr[2] = "Thomas" 
   document.write(arr.join())
```
##17、keys()从数组 fruit 创建一个数组迭代对象， 该对象包含了数组的键：如果对象是数组返回 true，否则返回 false。
```
    var a=[1,2,3]
    a.keys()
```

##18、lastIndexOf() 方法可返回一个指定的字符串值最后出现的位置，在一个字符串中的指定位置从后向前搜索。
```
    arr.join()
    str.lastIndexOf("Hello")
```
##19、map() 方法返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值。函数f中写具体的业务逻辑。
```
    var a1 = [1, 2, 3, 4];
    ar a2=a1.map(function f())
```
##20、pop() 方法用于删除并返回数组的最后一个元素。执行完pop()后，数组长度-1，删除最后一个元素。赋值给item;
```
        var a = ["Lily","lucy","Tom"];
        var item = a.pop();

```
##21、push() 方法可向数组的末尾添加一个或多个元素，并返回新的长度。在数组a后面，追加两个新的元素。
```
        var a = ["Lily","lucy","Tom"];
        var count = a.push("Jack","Sean");
```
##22、reduce() 从前往后遍历数组。可以给定一个函数。写业务逻辑
```
    var a = [12, 34, 34, 342, 345, 34, 123, 345, 45, 12]
    var newArr = a.reduce(function (){})
```
##23、reduceRight() 方法的功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前遍历。
```
    var a = [12, 34, 34, 342, 345, 34, 123, 345, 45, 12]
    var newArr = a.reduceRight(function (){})
```
##24、reverse() 方法用于颠倒数组中元素的顺序。
```
    var arr = new Array(3)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    
    document.write(arr + "<br />")
    document.write(arr.reverse())
```
##25、shift() 方法用于把数组的第一个元素从其中删除，并返回第一个元素的值。
```
    var arr = new Array(3)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    
    document.write(arr + "<br />")
    document.write(arr.shift() + "<br />")
    document.write(arr)
```
##26、slice() 方法可从已有的数组中返回选定的元素。返回一个新的数组，包含从 start 到 end （不包括该元素）的 a 中的元素。
```
    var a = [1, 2, 3, 4, 5];
    var b=a.slice(start,end)    
```
##27、some() 方法用于检测数组中的元素是否满足指定条件（函数提供）,函数f中可以写指定条件
```
     var a = [1, 2, 3, 4, 5];
     console.log(a.some(function f(){}));
            
       
```
##28、sort() 方法用于对数组的元素进行排序。元素可以是数字，也可以是字符串，
```
    var arr = new Array(6)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    arr[3] = "James"
    arr[4] = "Adrew"
    arr[5] = "Martin"
    
    document.write(arr + "<br />")
    document.write(arr.sort())
```
##29、splice() 方法向/从数组中添加/删除项目，然后返回被删除的项目。
```
    var arr = new Array(6)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    arr[3] = "James"
    arr[4] = "Adrew"
    arr[5] = "Martin"
    
    document.write(arr + "<br />")
    arr.splice(2,0,"William")
    document.write(arr + "<br />")
```
##30、toLocaleString()把数组转换为本地字符串。
```
    var arr = new Array(3)
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    
    document.write(arr.toLocaleString())
```
##31、toString() 方法可把一个逻辑值转换为字符串，并返回结果。
```
       var boo = new Boolean(true)
       document.write(boo.toString())
```
##32、unshift() 方法可向数组的开头添加一个或更多元素，并返回新的长度
```
    var arr = []
    arr[0] = "George"
    arr[1] = "John"
    arr[2] = "Thomas"
    
    document.write(arr + "<br />")
    document.write(arr.unshift("William") + "<br />")
    document.write(arr)   
```
##33、values() 方法返回一个新的 Array Iterator 对象，该对象包含数组每个索引的值
```
    
```

