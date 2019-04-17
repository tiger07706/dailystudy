# go学习笔记
## 一、极客时间《Go并发编程实战》
  郝林《Go并发编程实战》作者，前轻松筹大数据负责人
### 1、数组array和切片slice的区别
> array是**固定长度**的数组，使用前必须确定数组长度。
``
var arr[10] int;
var arr[10][10] int;
``
**数组array**的特点：
1、将一个数组赋值给另外一个，会拷贝所有的元素。
2、将数组做参数传递给函数时，将收到一个数组的拷贝，**而不是指针**。
3、**数组长度是其类型的一部分，**类型[10]int和[20]int是不同的。

> slice是对数组对抽象。切片slice的长度不固定，可以追加元素。
定义的方式
``
var slice1 []type = make([]type, len)
可以简写成
slice1 := make([]type, len)
也可以指定容量，其中capacity为可选参数
make([]T, length, capacity)
``
