#数组中的属性和方法
##1.concat  
- 将多个数组拼接成一个数组
``````
         var arr1=[1,2]
         var arr2=[3,4]
         var arr=arr1.concat(arr2)
         console.log(arr)
         
         输出：(4) [1, 2, 3, 4]

``````      
##2.constructor 
- 返回对创建此对象的数组函数的引用。
``````
        var test=new Array();
        
        if (test.constructor==Array){
         document.write("This is an Array");
         }
        if (test.constructor==Boolean) {
        document.write("This is a Boolean");
        }
        
        输出;This is an Array
``````
##3.copyWithin 
- 在当前数组内部，将指定位置的成员复制到其他位置（会覆盖原有成员），然后返回当前数组。
- 也就是说，使用这个方法，会修改当前数组。
- 用法：Array.prototype.copyWithin(target, start = 0, end = this.length)  
``````
        //将 3 号位复制到 0 号位  
       
       法一：
        arr=[1, 2, 3, 4, 5].copyWithin(0, 3, 4)
        console.log(arr)
      
       法二：
       arr= [1, 2, 3, 4, 5].copyWithin(0, -2, -1) 
       // -2 相当于 3 号位内容， -1 相当于 4 号位内容

       输出： [4, 2, 3, 4, 5]  
``````
##4.entries
- 从数组中创建一个可迭代对象， 该对象包含了数组的键值对
``````
        var arr = ["张三", "李四", "王五"];
        arr.entries();
        console.log(arr)
        
           输出：
                0: "张三"
                1: "李四"
                2: "王五"
                length: 3
``````
##5.every
- 用于检测数组所有元素是否都符合指定条件
    - 如果数组中检测到有一个元素不满足，则整个表达式返回 false ，且剩余的元素不会再进行检测。
    - 如果所有元素都满足条件，则返回 true。
``````   
        function min(arr) {
             return arr>4;
        }
        function main() {
             console.log(arr4.every(min))
        }
         main()
         
         输出： false
                  
         var arr4=[19,4,5,6,4,4]
              function min(arr) {
              return arr>3;
         }
         function main() {
              console.log(arr4.every(min))
         }
         main()
         
         输出：true
``````
##6.fill
- 使用固定值填充数组
``````
         var arr = ["a", "b", "c", "d"];
         arr.fill("aaa");
         console.log(arr)
         
         输出：["aaa", "aaa", "aaa", "aaa"]
``````
##7.filter
- 将所有元素进行判断，将满足条件的元素作为一个新的数组返回
``````
       var arr=[1,2,13,5,66]
          document.write(arr.filter(function(value,index,arr){
              return value>10
          }))
        
        输出：13,66
``````
##8.find
- 查找出第一个符合条件的数组成员，并返回该成员，如果没有找到就返回undefine
``````
        获取数组中年龄大于 18 的第一个元素
        
        var ages = [3, 10, 18, 20];
         
        var arr=[3,10,18,20]
        document.write(arr.find(function(value,index,arr){
        	return value<10
        }))
        输出:3
``````
##9.findIndex
-找到的是位置，找不到返回 -1

        var arr=[3,10,18,20]
        document.write(arr.findIndex(function(value,index,arr){
        	return value<10
        }))
        fruits 输出结果：0


##10.flat
- 该方法可以将嵌套数组进行扁平化处理成一维数组,
``````
       var arr= [1, 2, [3, 4, [5, 6]]];
       arr.flat(2);
       console.log(arr)
       
       输出：(3) [1, 2, Array(3)]
``````
##11.flatMap
- 该方法首先使用映射函数映射每个元素，然后将结果压缩成一个新数组。它与map和深度值1的flat几乎相同，但 flatMap通常在合并成一种方法的效率稍微高一些。
``````
        var arr1 = [1, 2, 3, 4];
     
        arr1.flatMap(x => [x * 2]);
        输出：[2, 4, 6, 8]
        
        let arr = ["今天天气不错", "", "早上好"]
        
        arr.map(s => s.split(""))
        // [["今", "天", "天", "气", "不", "错"],[],["早", "上", "好"]]
        
        arr.flatMap(s => s.split(''));
        // ["今", "天", "天", "气", "不", "错", "早", "上", "好"]
``````
##12.forEach
- 将数组中的每个元素执行传进提供的函数，没有返回值，直接改变原数组
``````
        var arr = [1, 2, 3];
           arr.forEach(function(element) {
               document.write(element);
           })
         
        输出：1,2,3
``````
##13.includes
- 检测数组中是否包含某元素
``````
        var site = ['a', 'ab', 'c'];
        site.includes('a'); 
        输出：true 
        site.includes('aa'); 
        输出：false
``````
##14.indexOf
- 查找数组中的某元素索引
``````
        var arr = ["a", "b", "c", "d"];
        var a = arr.indexOf("b");
        console.log(a)
        结果输出：1
``````
##15.join
- 把数组的所有元素放入一个字符串。元素通过指定的分隔符进行分隔。
``````        
         var arr = [1, 2, 3, 4, 5];
         var str = arr.join('*')
         console.log(str)
  
          输出：1*2*3*4*5
``````    
##16.keys
- 用于从数组创建一个包含数组键的可迭代对象。如果对象是数组返回 true，否则返回 false。
`````` 
        var fruits = ["b", "o", "a", "m"];
           fruits.keys();
           console.log(fruits)
        
        输出： ["b", "o", "a", "m"]
            0: "b"
            1: "o"
            2: "a"
            3: "m"
`````` 
##17.lastIndexOf
- 可返回一个指定的元素在数组中最后出现的位置，从该字符串的后面向前查找。如果要检索的元素没有出现，则该方法返回 -1。
``````
        var arr = ["a", "b", "c", "d"];
        var a = arr.lastIndexOf("c");
        输出：2
``````
##18.map
- 将数组中的每个元素调用一个提供的函数，结果作为一个新的数组返回，并没有改变原来的数组
``````
        var arr = [1, 2, 3, 4, 5]
        var newArr = arr.map(x => x*2)
        输出：arr= [1, 2, 3, 4, 5]   原数组保持不变
        输出：newArr = [2, 4, 6, 8, 10] 返回新数组
``````

##19.pop
- 在数组后面删除最后一个元素，并返回数组，此方法改变了数组的长度：
``````  
        var arr = [1, 2, 3, 4, 5]
        arr.pop()
        console.log(arr) 
        输出：[1, 2, 3, 4]
        console.log(arr.length) 
        输出：4
``````
##20.push
- 向数组的末尾添加一个或更多元素，并返回新的长度。
``````
        var arr=[1,2,3]
        arr.push(4)
        console.log(arr)
    
        输出：(4)[1,2,3,4]
``````
##21.reduce
- 所有元素调用返回函数，返回值为最后结果,传入的值必须是函数类型：
``````
        var arr = [1, 2, 3, 4]
        
        var sum = function(a, b) {
            console.log(a, b);
            return a + b
        }
        
        arr.reduce(sum) // => 10
        
        // 1 2
        // 3 3
        // 6 4
        输出：sum = 10 相当于累加的效果
``````
##22.reduceRight
- 该方法的功能和 reduce() 功能是一样的，不同的是 reduceRight() 从数组的末尾向前将数组中的数组项做累加。
``````
         var numbers = [65, 44, 12, 4];
          
         function getSum(total, num) {
             return total + num;
         }
         function myFunction(item) {
             document.getElementById("demo").innerHTML = numbers.reduceRight(getSum);
         }
         输出结果：125
``````
##23.reverse
- 颠倒数组中元素的顺序
``````
        var arr=["a","b","c"]
        document.write(arr + "<br />")
        document.write(arr.reverse())
        
        输出：
            a b c
            c b a
``````
##24.shift
- 在数组后面删除第一个元素，并返回数组，此方法改变了数组的长度：
``````    
        var arr = [1, 2, 3, 4, 5]
        arr.shift()
        console.log(arr) 
        输出：[2, 3, 4, 5]
        console.log(arr.length) 
        输出：4 
`````` 
##25.slice
- 从某个已有的数组返回选定的元素
``````     
        var arr=["a","b","c"]
        document.write(arr.slice(1) + "<br />")
        
        输出：b,c
``````  
##26.some
- 将所有元素进行判断返回一个布尔值，如果存在元素都满足判断条件，则返回true，若所有元素都不满足判断条件，则返回false：
``````    
          arr=[1,2,3,11]
          function compare(arr) {
              return arr>10
          }
          function my() {
              console.log(arr.some(compare))
          }
          my()
          
          输出true
``````  
##27.sort
- 对数组的元素进行排序
``````
        var arr=[5,7,1,4,2]
        arr.sort(arr);//1,2,4,5,7
  
        arr3=["a","c","e","g","d","b","f"]
        arr3.sort()
        console.log(arr3)// a,b,c,d,e,f,g
  
        arr4=[1,30,20,5,7,12]
        arr4.sort(function (a,b) {
              return a-b
        })
        console.log(arr4)//1,5,7,12,20,30
``````        
##28.splice
- 删除元素，并向数组添加新元素。万能方法，可以实现增删改：Array.splice(开始位置， 删除的个数，元素)
 ``````      
       var arr = [1, 2, 3, 4, 5];
       var arr1 = arr.splice(2, 0 'haha')
       var arr2 = arr.splice(2, 3)
       var arr3 = arr.splice(2, 1 'haha')
       console.log(arr1) //[1, 2, 'haha', 3, 4, 5]新增一个元素
       console.log(arr2) //[1, 2] 删除三个元素
       console.log(arr3) //[1, 2, 'haha', 4, 5] 替换一个元素
 `````` 
##29.toLocaleString
- 把数组转换为本地字符串
``````
        arr=["a","c","e"]
        document.write(arr.toLocaleString())
        输出：a,c,e
``````
##30.toString
- 把数组转换为字符串，并返回结果。
        var arr = [1, 2, 3, 4, 5];
        var str = arr.toString()
        console.log(str)
        输出：1,2,3,4,5
##31.unShift
- 将一个或多个元素添加到数组的开头，并返回新数组的长度：
``````        
        var arr = [1, 2, 3, 4, 5]
        arr.unshift(6, 7)
        console.log(arr) 
        输出：[6, 7, 2, 3, 4, 5]
        console.log(arr.length)
        输出：7
`````` 
##32.values
- 返回数组对象的原始值
``````
        var arr = ['w', 'y', 'k', 'o', 'p'];
        var eArr = arr.values();
        // 您的浏览器必须支持 for..of 循环
        // 以及 let —— 将变量作用域限定在 for 循环中
        for (let letter of eArr) {
          console.log(letter);
        }
        输出：w y k o p
``````
##33.Symbol(Symbol.iterator)
- 指定为对象的默认迭代器。使用for...of
``````       
        var str = "",arr = [],num = 2;
     
         console.log(str[Symbol.iterator]);//[Symbol.iterator]()
         console.log(arr[Symbol.iterator]);//[Symbol.iterator]()
         console.log(num[Symbol.iterator]);//undefined
`````` 
##34.Symbol(Symbol.unscopables)
- 指用于指定对象值，其对象自身和继承的从关联对象的 with 环境绑定中排除的属性名称。
``````
           var obj = {
                  foo: 1,
                  bar: 2
              };
          
              obj[Symbol.unscopables] = {
                  foo: false,
                  bar: true
              };
          
              with(obj) {
                  console.log(foo); // 1
                  console.log(bar); // ReferenceError: bar is not defined
              }
``````