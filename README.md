## js高级程序设计笔记
### 一、js数据类型
基本类型为：Number,String,Boolen,Null.Undefined.
引用类型：Object,Array,Date,RegExp(正则),Function.

- 检测数组的方法
instance of 检测传入值的原型
Array.idArray()方法，确定某个值是不是数组
- 转换方法
所有对象都具有toLocaleString(),toString(),valueOf()方法
1. toString()方法会返回由数组中每个值的字符串形式拼接而成的一个以逗号分隔的字符串
2. valueOf()返回的还是数组
3. toLocaleString()会创建一个数组值的以逗号分隔的字符串
- 栈方法
js中的数组可以像栈一样后进先出（LIFO），主要体现在pop()与push()方法，pop()方法可以将数组数组末尾的数移除，并返回移除的项。push()方法可以将任意数量的参数添加到数组末尾，返回修改后数组的长度。
- 队列方法
js的数组也可以模仿队列先进先出(FIFO)，主要体现在shift()与push()方法。shift()方法可以移除数组中的第一个数，并返回移除的项，数组长度减一。
- 重排序方法
分为sort()与reverse()方法。reverse()方法会反转数组的顺序，sort()方法默认升序排列，会默认调用toString()转型方法，比较得到的字符串排序。一般使用为
array.sort((a, b) => a - b)
- 操作方法
cancat()方法会创建一个当前数组的副本，然后将接收到的参数添加到副本数组的末尾并返回副本。
slice()方法会基于当前数组中的一个或多个项创建一个新数组。接收一或两个参数，start和end，即开始位置与结束位置，以数组序号为准。slice()方法并不会改变原数组。
splice()方法可以对原数组进行删除、插入、替换的操作，主要依据接受的参数个数。
1. 删除：指定两个参数即起始位置，删除的个数。
2. 插入：指定三个参数即起始位置，0，要插入的数据。
3. 替换：指定三个参数即起始位置，删除项数，要插入的数据。
splice()方法始终都会返回一个数组，包含从原数组中删除的项。
- 位置方法
indexOf()与lastIndexOf()方法，两个方法都接受两个参数：要查找的项和表示查找起点位置的索引。indexOf()方法会从数组的开头向后查找，lastIndexOf()会从数组末尾向前查找。
两个方法都会返回要查找的项在数组中的位置，没找到的情况下返回-1.在进行比较操作时，会使用全等操作符即类型与值的比较。