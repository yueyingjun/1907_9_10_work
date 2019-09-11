
# concat
##concat() 方法用于连接两个或多个数组。该方法不会改变现有的数组，而仅仅会返回被连接数组的一个副本。
 -语法：arrayObject.concat(arrayX,arrayX,......,arrayX)
```
var a = [1,2,3];
document.write(a.concat(4,5));
[1,2,3.4.5]
```
#Array
-Array 对象用于在单个的变量中存储多个值。,
-constructor 属性返回对创建此对象的数组函数的引用。
```

function employee(name,job,born)
{
this.name=name;
this.job=job;
this.born=born;
}
var bill=new employee("Bill Gates","Engineer",1985);
document.write(bill.constructor);
```
function employee(name, job, born)
{this.name = name; this.job = job; this.born = born;}

#length
-length 属性可设置或返回数组中元素的数目。
-
```
var arr = new Array(3)
arr[0] = "John"
arr[1] = "Andy"
arr[2] = "Wendy"

document.write("Original length: " + arr.length)
document.write("<br />")

arr.length=5
document.write("New length: " + arr.length)
```
Original length: 3
New length: 5 

#copyWithin
-复制数组的前面两个元素到后面两个元素上：copyWithin() 方法用于从数组的指定位置拷贝元素到数组的另一个指定位置中
```var fruits = ["Banana", "Orange", "Apple", "Mango"];
   fruits.copyWithin(2, 0);
   ```
   Banana,Orange,Banana,Orange
   
   #
