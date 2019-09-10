# 数组笔记
## 数组方法
- concat() ：合并两个或多个数组
```
        var arr1 = [1,2,3]
        var arr2 = [4,5,6]
        var arr3 = ["a","b","c"]
        console.log(arr1.concat(arr2))
        console.log(arr1.concat(arr2,arr3))
        
        (6) [1, 2, 3, 4, 5, 6]
        (9) [1, 2, 3, 4, 5, 6, "a", "b", "c"]
```

- constructor()(构造函数) ：表示创建对象的函数
```$xslt
        var arr = ["a","b","c"]
        var str = "a,b,c"
        console.log(arr.constructor)
        console.log(str.constructor)
        
        ƒ Array() { [native code] }
        ƒ String() { [native code] } 
```

- Array(): 新建一个数组  
```$xslt
        var arr1 = new Array();//新建一个空数组
        var arr2 = new Array(5);//新建一个长度为20位的空数组
        var arr3 = new Array("1","2");//新建一个内容包括有1，2两位的数组
        console.log(arr1)
        console.log(arr2)
        console.log(arr3)
        
        []
        (5) [empty × 5]
        (2) ["1", "2"]
```

- isArray()： 判断一个对象是否为数组。
```$xslt
        var arr = [1,2,3,4];
        var str = "1,2,3,4"
        console.log(Array.isArray(arr))
        console.log(Array.isArray(str))
        
        true
        false
```

- copyWithin():  在数组内部，将一段元素序列拷贝到另一段元素序列上，覆盖原有的值
```$xslt
        var arr1 = [1,2,3,4];
        arr1.copyWithin(3,1);
        console.log(arr1)
        
     
        (4) [1, 2, 3, 2] //把下标为1的元素（2）复制，替换下标为3的元素（4）
```

-fill():将数组中指定区间的所有元素的值，都替换成某个固定的值。
```$xslt
        var arr = [1,2,3,4];
        console.log(arr.fill(10))//替换数组中的所有元素
        
        (4) [10, 10, 10, 10]
        
```

- filter(): 创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。
```$xslt
        var arr = [1,2,3,4];
        function f(arr) {
            return arr <3;
        }
        console.log(arr.filter(f))//输出数组中所有满足条件的元素
        
        (2) [1, 2]
```

- find(): 返回通过测试（函数内判断）的数组的第一个元素的值。
```$xslt
        var arr = [1,2,3,4];
        function f(arr) {
            return arr <3;
        }
        console.log(arr.find(f))//输出第一个满足条件的值
        
        1
```

- findIndex() :返回传入一个测试条件（函数）符合条件的数组第一个元素位置。
```$xslt
        var arr = [1,2,3,4];
        function f(arr) {
            return arr <3;
        }
        console.log(arr.findIndex(f))//输出第一个满足条件的值的下标
        
        0

```

- entries(): 返回一个数组的迭代对象，该对象包含数组的键值对 (key/value)。
- - 迭代对象中数组的索引值作为 key， 数组元素作为 value。
```$xslt
        var fruits = [1，2，3，4];
        fruits.entries();
        
        [0, 1]
        [1, 2]
        [2, 3]
        [3, 4]
```

-  every(): 检测数值元素的每个元素是否都符合条件。
```$xslt
        var arr = [1,2,3]
        function checkAdult(arr) {
         return arr >= 10;  //return arr < 10;  返回true
        }
        console.log(arr.every(checkAdult))

        false
```

- forEach() :调用数组中的每个元素，把元素传给回调函数(遍历数组)
```$xslt
        var arr = [1,2,3,4];
        arr.forEach(function (i, index, array) {
            console.log(i, index)
        })
```

- keys() :从数组创建一个包含数组键的可迭代对象。
```$xslt
        var arr = ['a', 'b', 'c'];
        var iterator = arr.keys();
        console.log(iterator.next());
        
        谷歌浏览器运行结果
        {value: 0, done: false}
        done: false
        value: 0
        IE浏览器运行结果
        [object Object]
```

- map():返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值。
```$xslt
        var arr1 = [1, 2, 3, 4];
        const m1 = arr1.map(x => x * 2);
        console.log(m1);
        
        (4) [2, 4, 6, 8]
```

- reduce():接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值。
```$xslt
        const arr = [1, 2, 3, 4, 5]
        var sum = arr.reduce(function(total,currentValue){
            return total+currentValue;
        });
        console.log(sum)
        
        15

```

- reduceRight(): 方法的功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前将数组中的数组项做累加。
```$xslt
        const arr = [1, 2, 3, 4, 5]
        var sum = arr.reduceRight(function(total,currentValue){
            return total+currentValue;
        });
        console.log(sum)
```

- values() :返回一个数组迭代器对象，该迭代器会包含所有数组元素的值。
```$xslt
        const arr = ['a', 'b', 'c'];
        const iterator = arr.values();
        for (const value of iterator) {
            console.log(value);
        }
        
        a
        b
        c
```

- from() ：用于通过拥有 length 属性的对象或可迭代的对象来返回一个数组。(创建一个新数组)
```$xslt
        console.log(Array.from('abcdef'));
        
        (6) ["a", "b", "c", "d", "e", "f"]
```

- includes(): 用来判断一个数组是否包含一个指定的值，如果是返回 true，否则false。
```$xslt
        var arr = [1,2,3,4];
        console.log(arr.includes(2))
        console.log(arr.includes("a"))
        
        true
        false
```

- indexOf() :返回数组中第一个与指定值相等的元素的索引，如果找不到这样的元素，则返回 -1。
```$xslt
var arr = [1,2,3,4];
        console.log(arr.indexOf(3))
        console.log(arr.indexOf(10))
        
        2
        -1
```

- lastIndexOf() ：返回数组中最后一个（从右边数第一个）与指定值相等的元素的索引，如果找不到这样的元素，则返回 -1。
```$xslt
        var arr = [1,2,3,2,3,1,1,2,3,3];
        console.log(arr.lastIndexOf(1))
        console.log(arr.lastIndexOf(0))
        
        6
        -1
```

- some() ：如果数组中至少有一个元素满足测试函数，则返回 true，否则返回 false。
```$xslt
        var arr = [1, 2, 3, 4, 5];
        function f(num) {
            return num == 0; //return num %2 == 0;返回true
        };
        console.log(arr.some(f));
        
        false
```

- sort() ：用于对数组的元素进行排序。
```$xslt
        var arr = [2, 9, 0, 1, 5];
        console.log(arr.sort());
        //有问题，只比较了第一位数字
        var arr = [2, 9, 20, 11, 5];
        console.log(arr.sort())
        
        (5) [0, 1, 2, 5, 9]
        (5) [11, 2, 20, 5, 9]
```

- reverse():用于颠倒数组中元素的顺序。
```$xslt
        const arr = [1, 2, 3, 4];
        console.log(arr.reverse())
        
        (4) [4, 3, 2, 1]
```

- join():把数组中的所有元素转换一个字符串。
```$xslt
        var arr = [1,2,3,4];
        console.log(arr.join())
        
        1,2,3,4
```

- toString() :可把数组转换为字符串，并返回结果。
```$xslt
        var arr = [1,2,3,4,5];
        console.log(arr.toString())
        
        1,2,3,4,5
```

- toLocaleString() :返回一个由所有数组元素组合而成的本地化后的字符串
```$xslt
        var arr = [1, 'a', Date('Dec 1997 14:12:00 ')];
        var localeString = arr.toLocaleString();
        console.log(localeString);
        
        1,a,Wed Sep 11 2019 00:56:34 GMT+0800 (中国标准时间)

```

- slice():抽取当前数组中的一段元素组合成一个新数组。可提取字符串的某个部分，并以新的字符串返回被提取的部分。
```$xslt
        const arr = ["a","b","c","d","e"];
        console.log(arr.slice(2))//截断下标前面的元素，从当前下标的元素开始之后的元素合成新数组
        console.log(arr.slice(0,2))//从第一位下标开始到第二位下标的前一位
        console.log(arr.slice(2,4))
        
        (3) ["c", "d", "e"]
        (2) ["a", "b"]
        (3) ["c", "d", "e"]

```

splice() :用于添加或删除数组中的元素。
```$xslt
        var arr = [1,2,3,4,5];
        arr.splice(1, 0, 6);//第一位表示下标 第二位表示从第一位下标的前一位开始往后要删除的个数，第三位表示从第一位下标的前一位开始往后要插入的元素
        console.log(arr);
        arr.splice(3,3)
        console.log(arr);
        
        (6) [1, 6, 2, 3, 4, 5]
        (3) [1, 6, 2]
```

- shift():把数组的第一个元素从其中删除，并返回第一个元素的值。
```$xslt
        const arr = [2, 1, 3, 4];
        console.log(arr.shift(2))
        console.log(arr)
        
        2
        (3) [1, 3, 4]
```

- unshift() :在数组的开头增加一个或多个元素，并返回数组的新长度。
```$xslt
        var arr = [1,2,3,4,5];
        console.log(arr.unshift(6))
        console.log(arr)
        console.log(arr.unshift(7,8,9))
        console.log(arr)
        
        6
        (6) [6, 1, 2, 3, 4, 5]
        9
        (9) [7, 8, 9, 6, 1, 2, 3, 4, 5]
```

- push(): 在数组的末尾增加一个或多个元素，并返回数组的新长度。
```$xslt
        var arr1 = [1, 2, 3, 4];
        console.log(arr1.push(66))
        console.log(arr1)
        
        1
        2
        3
        4
        5
        (5) [1, 2, 3, 4, 66]
```

- pop():删除数组的最后一个元素，并返回这个元素。
```$xslt
        var arr = [1,2,3,4];
        console.log(arr.pop())
        console.log(arr);
        
        4
        (3) [1, 2, 3]
```


